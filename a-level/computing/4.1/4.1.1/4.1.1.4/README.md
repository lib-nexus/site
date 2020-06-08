## Topic Quota

> Be familiar with and be able to use
> * equal to
> * not equal to
> * less than
> * greater than
> * less than or equal to
> * greater than or equal to

## Relational operations in a programming language

Because our programming language is python, we'll write examples in python. Expressions in the topic quota or evaluative operators which means that they evaluate an expressions. They are self explanatory. `{expression} {operator} {expression}` is the syntax in which they are implemented, it evaluates the expression from left to right. To display these, we can make a few python `if` statements. The list of the operators in relation to their technical name is listed as follows

* `==` equal to
* `!=` not equal to
* `<` less than
* `>` greater than
* `<=` less than or equal to
* `>=` greater than or equal to

```python

class My:

    Name = 'Quentin'
    Age = 16

if My.Name == 'Quentin': # Checks if the attribute Name from class My has the content of the right hand side

    print('My name is Quentin')

if My.Name != 'Quentin': # Checks if the attribute Name from class My has not got the content of the right hand side

    print('My name is not Quentin')

if My.Age < 16: # Checks if the attribute Name from class My is less than the ( in this case ) integer value of the right hand side

    print('I\'m younger than 16')

if My.Age > 16: # Checks if the attribute Name from class My is greater than the ( in this case ) integer value of the right hand side

    print('I\'m older than 16')

if My.Age <= 16: # Checks if the attribute Name from class My is less than or equal to the ( in this case ) integer value of the right hand side

    print('I\'m younger than or 16')

if My.Age >= 16: # Checks if the attribute Name from class My is greater than or equal to the ( in this case ) integer value of the right hand side

    print('I\'m older than or 16')

```

The operators `==` and `!=` accept all types, as they both evaluate a literal value. However when evaluating an amount, we need either an `int` or a `float`. When we get to pointers and referencing, we can look at the `is` operator. ( If you can't wait, it just evaluates what space a pointer points to ).