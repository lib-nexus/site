## Topic Quota

> Be familiar with and be able to use
> * NOT
> * AND
> * OR
> * XOR


## Boolean operations in a programming language

In python, all of the above operators are implemented so that programming are able to have boolean functionality. Boolean logic is used in logic gates and can be easily explained in python, since it's supposed to be boolean operations in a programming language. Before we start i'm going to define some variables for use in later code snippets.

### NOT

```python
if not True:

    print('The expression is false') # Doesn't run

if not False:

    print('The expression is false') # Does run
```

Because point1 has the value of `True`, it is not false. Because the `not` operator wants the expression to be `False`, this means that the print statement won't run, because once again, point1 is `True`. However in point2's case, it has the value of `False` and because the `not` operator wants `False` expression, it will run.

### AND

```python
if True and True:

    print('Both expressions are true') # Does run

if True and False:

    print('Both expressions are true') # Doesn't run
```

Because point1 and point2 both have the value `True`, both expressions either side are `True`. However when it comes to point3 and point4, because both expressions aren't `True`, the print statement doesn't get to be run.

### OR

```python
if True or False:

    print('Either expression is true') # Does run

if False or False:

    print('Either expression is true') # Doesn't run
```

Because point2 is `False` but point1 is `True` the print statement does run. This is because the `or` operator wants either expression to be true. However point3 and point4 are both `False` and because neither of them are true, the print statement doesn't run.

### XOR

```python
if True ^ False:

    print('Expression 1 is not equal to Expression 2') # Does run

if True ^ True:

    print('Expression 1 is not equal to Expression 2') # Doesn't run

# LIKEWISE, YOU COULD USE AND NOT

if True and not False:

    print('Expression 1 is not equal to Expression 2') # Does run

if True and not True:

    print('Expression 1 is not equal to Expression 2') # Doesn't run
```

Because point1 is `True` and point2 is `False` ( Neither expression has the same value as the other ). The first print statement can be run. This is because the `^` ( XOR ) operator wants it's expressions to not have the same value. And so of course the reverse for point3 and point4 because both values do have the same value. The last 2 print statements are invoked the same as the former two but instead of using the `^` operator, it uses `and not` which basically does the same thing.

Now that that's finished, can you figure out what the following statements' output's would be?

> ```python
> not True and not True and False or True and not False and not True
> True and not False or True ^ False and not False
> True and not not False and True or False and True and not True and
> False and not True ^ False and True or True and not False
> ```