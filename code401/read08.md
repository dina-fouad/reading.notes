## List Comprehensions in Python :

It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

```
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))
```

## Syntax
The list comprehension starts with a ‘[‘ and ‘]’, square brackets, to help you remember that the
result is going to be a list.

The basic syntax uses square brackets.

[ expression for item in list if conditional ]
```
This is equivalent to:

for item in list:
    if conditional:
        expression
```
Let’s break this down and see what it does.

 ```     
new_list = [expression(i) for i in old_list if filter(i)]
new_list
```
The new list (result).

expression(i)

- Expression is based on the variable used for each element in the old list.
```
for i in old_list
```
The word for followed by the variable name to use, followed by the word in the
old list.

```
if filter(i)
```
- Apply a filter with an If-statement.

Create a list using loops and list comprehension
For the next example, assume we want to create a list of squares. Start with an empty list.

# You can either use loops:
squares = []

for x in range(10):
    squares.append(x**2)
 
print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Or you can use list comprehensions to get the same result:
squares = [x**2 for x in range(10)]

print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]