# Learn Bash Scripting by Building Five Programs

From: freeCodeCamp
Tags: Bash scripting, SQL
cert: no

### Key words | Questions

### Notes

`help <command/expression>`

```bash
which bash 
```

That's the absolute path to the bash interpreter. You can tell your program to use it by placing a shebang at the very top of the file like this: `#!<path_to_interpreter>`. Add a shebang at the very top of your file, the one you want looks like this:

```bash
#!/bin/bash

#./filename - execute
```

## Vars

```bash
VAR="value"

echo $VAR
```

The question was printed. Next, you want to be able to accept input from a user. You can do that with read like this: read VARIABLE_NAME. This will get user input and store it into a new variable. After you print the question, use read to get input and store it in a variable named NAME.

```bash
read $NAME # read from input 
```

## Args

```bash
echo $* # all arguments 

echo $1 # first argument
```

## Conditions

```bash
if [[ CONDITION ]]
then
  STATEMENTS
fi
```

You can compare integers inside the brackets (`[[ ... ]]`) of your if with `-eq` (equal), `-ne` (not equal), `-lt` (less than), `-le` (less than or equal), `-gt` (greater than), `-ge` (greater than or equal). Change your if condition to check if your first argument is less than 5.

```bash
if [[ $1 == arg1 ]]
then
  echo true
else
  echo false  
fi

# ===

if [[ $1 -lt 5 ]]
then
  echo true
else
  echo false  
fi
```

<aside>
📌 **SUMMARY:**

</aside>