# Django main

#CSS #Django #HTML #Python #SQL

1. [[models]]
2. [[views]]
3. [[urls]]
4. [[admin]]

## migratinos
```sql
$ ./manage.py makemigrations # read APPS moderls.py and create/evolve migratinons 

$ ./manage.py migrate # create or alter database 

$ ./manage.py check
```

## Dig a little bit into object relational mapping
```python
from django.db import connection
print(connection.queries)
```

