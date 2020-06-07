## Topic Quota

> Be familiar with and be able to use
> * addition
> * subtraction
> * multiplication
> * real/float division
> * integer division, including remainders
> * exponentiation
> * rounding
> * truncation

## Arithmetic operations in a programming language

A mistake that i made on the previous page was use typescript to showcase the programing features as opposed to python which is the school's chosen language for taking the a-level examination. From now on, i will try my utmost to use python when it is doesn't interfere with getting the point across. So, below are examples of all arithmetic operations written in python with ( hopefully ) satisfying explanations.

In python, when we want to write an arithmetic expression, we do it like we would in real life, consequentially. These operators are as follows
* `+` Add
* `-` Minus
* `/` Divide
* `*` Multiply
* `**` To the power of / Exponentiate

```python
print(f'The formatted expression\'s value is {5 + 5 / 5 - 5 * 5 ** 5}')
```
This is the standard way that we add things to one another, of course, the amount of times you can add one value to another is unlimited like in standard maths. This isn't exclusive to presenting the expression in a print statement, we can use it anywhere, like in declaring a variable `x = 5 + 5 / 5`. 

You can use the above method in conjunction with variables, for example assuming we have already given `x` a value, `x = x + 3 / 2 * 1 ** 0`. When we want to do something to a value, like add something to it like in iteration. We can use assignment operators. These are limited to all but the `to the power of` operator. It would be `{variable}{operator}={expression}` for example `x += 10/3` would give `x` the value of adding `10/3` to itself. Or for another example `x /= 3` would  make `x` itself divided by 3.

Now we've covered the simple operators of python for covering addition, subtraction and multiplication. We can move on to explaining float division, integer division with remainders and then later move on to using subroutines for rounding and truncation.

When it comes to float division, it's just the same as normal division, except that when we divide something by something else, for safety, it's always best to expect a float value. This is much the same when it comes to integer division, however instead of getting python to give us a float value, we can ask for the remainder using a `remainder operator` which is `%`. For example `x = 5 % 4` would give `x` a value of 1 because we can divide 5 by 4 one time remainder one.

The subroutine for rounding is the standard `round()` function. Rounding is the operation of taking a look one decimal place past the expected decimal places for the rounding, and deciding to either add 1 to the last one or remove 1 from the last one depending on whether it's higher or lower than the aforementioned last expected decimal palce. For truncation, we can either use the `trunc()` function from the math library or make our own, we'll make our own one. Truncation is the operation of instead of rounding a number, cutting off all decimal places entirely.

```python
def truncate(val: float) -> int:

    return int(str(val).split('.')[0]) #We've turned the float into a string and then split that string by the decimal place. We've taken the first array item from that new list and turned it into a string
```