## [Home](http://lib-nexus.github.io/site) | [Docs](https://lib-nexus.github.io/site/docs) | [Blog](https://www.youtube.com/watch?v=dQw4w9WgXcQ) | [My Media](https://lib-nexus.github.io/site/my/media) | [My Projects](https://lib-nexus.github.io/site/my/projects)

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


### `BetterString.Endswith(String='Astring')`

### `BetterString.RegMatch(String='Astring')`

### `BetterString.Len() \ BetterString.Len`

### `BetterString.WriteTo(File='Afile.txt')`


### `BetterString.Shift(Set=True, Return=False, Points=10)`

### `BetterString.Shuffle(Set=True, Return=False)`

### `BetterString.Destroy()`
- STATUS: Not Available

### `BetterString.Caeser()`
- STATUS: Not Available

### `BetterString.Warp(Chance=0.001)`
- STATUS: Not Available

### `BetterString.Yeltsakcir()`
- STATUS: Not Available

### `Bettertring.CMD()`
- STATUS: Not Available
