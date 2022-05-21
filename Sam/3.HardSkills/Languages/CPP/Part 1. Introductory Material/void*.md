# void*
#types #cpp
We can point to [[nullptr]]
Used in low-level code for store or pass along an address of a memory location without actually knowing what type of object is stored there. 

It can be read like `void*` as "pointer to an object of unknown type" 

A pointer to any type of object can be assigned to a variable of type `void*`, but a pointer to function or a pointer to member cannot. In addition, a `void* `can be assigned to another `void*`, `void*s` can be compared for equality and inequality, and a `void*` can be explicitly converted to another type.

Other operations would be unsafe because the compiler cannot know what kind of object is really pointed to. Consequently, other operations result in compile-time errors. To use a `void*`, we must explicitly convert it to a pointer to a specific type.
- can't dereference `void*`
- can't increment `void*`, cuz size of the object pointed is unknown
 For example:
```cpp
void f(int∗ pi)
{
	void∗ pv = pi;  // ok: implicit conversion of int* to void*
	∗pv; // error: can’t dereference void*
	++pv; // error: can’t increment void* (the size of the object pointed to is unknown)
	int∗ pi2 = static_cast<int∗>(pv); // explicit conversion back to int*
	double∗ pd1 = pv; // error
	double∗ pd2 = pi; // error
	double∗ pd3 = static_cast<double∗>(pv); // unsafe (§11.5.2)
}
```

In general, it is not safe to use a pointer that has been converted (‘‘cast’’) to a type that
differs from the type of the object pointed to.  For example, a machine may assume
that every double is allocated on an 8-byte boundary. If so, strange behavior could
arise if pi pointed to an int that wasn’t allocated that way. This form of explicit type
conversion is inherently unsafe and ugly. Consequently, the notation used, 
 `static_cast`, was designed to be ugly and easy to find in code. The primary use for
`void∗` is for passing pointers to functions that are not allowed to make assumptions 
about the type of the object and for returning untyped objects from functions. To use
such an object, we must use explicit type conversion. Functions using `void∗` pointers
typically exist at the very lowest level of the system, where real hardware resources 
are manipulated.
For example:
```cpp
void∗ my_alloc(size_t n); // allocate n bytes from my special heap
```
Occurrences of `void∗s` at higher levels of the system should be viewed with great
suspicion because they are likely indicators of design errors. Where used for 
optimization, `void∗` can be hidden behind a type-safe interface Pointers to functions
and pointers to members cannot be assigned to `void∗s`.
