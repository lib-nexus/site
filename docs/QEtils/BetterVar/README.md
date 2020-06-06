## [Home](http://libnexus.github.io/site) | [Docs](https://libnexus.github.io/site/docs) | [Blog](https://www.youtube.com/watch?v=dQw4w9WgXcQ) | [Tutorials](https://libnexus.github.io/site/tutorials) | [A-Level](https://libnexus.github.io/site/a-level) | [Contact](https://libnexus.github.io/site/contact) | [Résumé](https://libnexus.github.io/site/résumé)

## The FileHandler docs

### Useful Links
- [Tutorial](#Tutorial)
- [BetterStringClass](#BetterStringClass)
- [BetterFloatClass](#BetterFloatClass)
- [BetterListClass](#BetterListClass)
- [BetterDictionaryClass](#BetterDictionaryClass)

On this page, you will find all the documentation you will likely need for navigating the `BetterVar` module. This module was made to add functionality the python doesn't readily have available for manipulation of different variables, the table of modules which currently are ready/in the update. In the event that it does not provide all information you need, please consult a Teacher or any other Mentioned Contributors of the Project. They can be found either on the web-page or by using the following code.
```python 
from QEtils.Information import Contributors
[print(Contributor.Name) for Contributor in Contributors()]
```

| Module | Ready | In Update | ApproxPerct |
| --- | --- | --- | --- |
| `BetterString` | Yes | No | 100% |
| `BetterFloat` | No | No | 0% |
| `BetterList` | No | No | 0% |
| `BetterDict` | No | No | 0% |

---

## Tutorial

### Before we begin

```python
#Use either of the following pieces of code
from QEtils.BetterVar import BetterString
#OR
import QEtils
```
## Creating our instance

To begin using the `BetterVar` library, we are going to want to create an instance of our variable. for this example i will be using the `BetterString` and will import the module directly using the former of the above code. To create my string, i'll use the following code

```python
MyString = BetterString('Hello World!')
```

## Using the BetterString

Now that we have our instance of the BetterString variable, we can use a bunch of different methods to manipulate the string. This is much better than the [Hello World](https://lib-nexus.github.io/site/docs/QEtils/HelloWorld) in my opinion! Some of these methods are as follows
```python
MyString.Shift(Set=True, Return=False, Points=10) #We don't need it to return a value, we just want it to set itself to it's shifted version. The poitns argument is how many characters over it will shift
print(f'{MyString == MyString.Shuffle()}, {MyString}, {MyString.Shuffle()}') #Now we'll just print out what a shuffled version of the MyString variable would look like as well as it's own  self thanks to '__str__'
```

The current possibilities to be used for the MyString variable are as follows
```python
MyString.Shuffle(Set=True, Return=False)
MyString.Shift(Set=True, Return=False, Points=10)

if MyString.Endswith('World'):
    print('How did i manage to get here?')

elif Match := MyString.RegMatch('([a-F]+)')[1]:

    print(f'We did it! The match was {Match}')
```

I'm afraid that since it's not like an environment, there's not much that can be taught in a tutorial which won't come easy to someone for this module so check out the BetterString 'practical' docs down below and start programming!

## BetterString
Note: Instead of choosing to use the format `def Foo(Astring: str, Abool: bool)` in my functions, i have decided to make a custom error message however this isn't always practical so wherever it applies, use the above syntax to make sure the variable value is the wanted one as opposed to how i do it.

### `BetterString(String='Astring')`
- Takes 1 argument
    - String: Defines the base/Starting value
- Creates an instance of the BetterString class for use creating a better string
- Returns `object`

### `BetterString.Endswith(String='Astring')`
- Takes 1 argument
    - String: This string is what will be used to check if something exists at the end of the betterstring value, No default value
- Using the parameter `String`, the method checks if String exists at the end of the variable's value. This was made because of python's lack of a `.endswith()` in terms of built-in functions
- Returns `boolean`

### `BetterString.RegMatch(MatchString='Astring', Warn=False)`
- Takes 2 arguments
    - MatchString: This paramater is what will be used for the r string in terms of finding out if the variable's value matches a certain regex, No default value
    - Warn: This decides whether or not to send a warning in the event that the python version of the module implementing this feature does not support the walrus operator, Default value is `True`
- Returns `tuple`:`boolean`, `string`/`None`
    
### `BetterString.Len() \ BetterString.Len`
- Takes no arguments
- This will get the current length of the variable's value
- Returns `String`

### `BetterString.WriteTo(File='Afile.txt', Mode='w')`
- Takes 2 arguments
    - File: This parameter isn't confined to a filename but a path, this is the path it takes to get to the file it writes to, No default value
    - Mode: This parameter chooses the mode which it will use to open the file, it only however takes the file writing protocols of `a`, `a+`, `w`, `w+`, Default value is `w`
- Returns `None`
- This method will take the value of the string variable

### `BetterString.Shift(Points=0, ReverseDir=False, Set=False, Return=True)`
- Takes 4 arguments
    - Points: This is the amount of characters that the string will be shifted by. It does not take any negative number, Default value is `0`
    - ReverseDir: This is the direction in which it is shifted, instead of attempting to use a negative value, use this, it takes a `Boolean`, Default value is `False`
    - Set: This decides whether or not to set the betterstring's current value to the outcome of the shift, takes a `Boolean`, Default value is `False`
    - Return: This decides whether or not the method returns something. Takes a `Boolean`, Default value is `True`
- This will shift the string value of the betterstring variable

### `BetterString.Shuffle(Set=True, Return=False)`
- Takes 2 arguments
    - Set: Decides whether or not to set the variable's current value to the outcome of the method, Default value is `True`
    - Return: Decides whether or not to Return the outcome of the method, Default value is `False`
- This shuffles the characters in the string to jump them up

### `BetterString.Change(String)`
- Takes 1 argument
    - String: This is the string that the variable's value will be change to, it asserts it as the new string value, No default value
- Changes the value of the betterstring object to the String parameter

### `BetterString.Destroy()`
- Takes no arguments
- This simply sets the value of the variable to a `NoneType` object

### `BetterString.Caeser()`
- STATUS: Not Available `Uses sherlock module`

### `BetterString.Warp(Lowerbound, Upperbound=100)`
- Takes 2 arguments
    - Lowerbound: The lowerbound for calculating the chance that the string will warp, No default value
    - Upperbound: The upperbound for calculating the chance that the string will warp, Default value is 100
- Using the chance parameter, this method will shuffle it's contents if the integer between the Upper and Lower bounds is the lower bound, it will change the string

### `BetterString.Yeltsakcir()`
- Takes no arguments
- This is a joke method, it will change your variable's value

### `Bettertring.CMD()`
- STATUS: Not Available
