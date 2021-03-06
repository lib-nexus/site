## [Home](http://libnexus.github.io/site) | [Docs](https://libnexus.github.io/site/docs) | [Blog](https://www.youtube.com/watch?v=dQw4w9WgXcQ) | [Tutorials](https://libnexus.github.io/site/tutorials) | [A-Level](https://libnexus.github.io/site/a-level) | [Contact](https://libnexus.github.io/site/contact) | [Résumé](https://libnexus.github.io/site/résumé)

## The FileHandler docs

### Useful Links
- [Tutorial](#Tutorial)
- [FileHandlerClass](#FileHandlerClass)

Here you will find (hopefully) all the information you're looking for when tring to use the FileHandler class from QEtils, in the event that it does not however have all information you need, please consult a Teacher or any other Mentioned Contributors of the Project. They can be found either on the web-page or by using the following code.
```python 
from QEtils.Information import Contributors
[print(Contributor.Name) for Contributor in Contributors()]
```
---
## Tutorial

### Before we begin

```python
#Use the following code at the top of your page, this will import only the FileHandler library
from QEtils import FileHandler
```
## Creating our instance

To begin using the filehandler, you will want to create an instance of the class, this can be done by assigning it to a variable, below i've named my variable `myfile` and given it the following arguments
```python
myfile = FileHandler(File="ThisThing.txt")
```

## Using the FileHandler methods

As you can see i have specified what attribute i am giving a value to. Anothing argument i could have passed through the FileHandler class was the `Path` argument. This arguments allows me to specify what directories to go to/through to get to the main file, specified as `File` this doesn't need to be done however because i am fine with making the file appear just where i run my python code!
Now i have a few options with what i can do, but i will start by creating the file with the pathname and file i have specified
```python
myfile.Create()
```
Because myfile is an instance of FileHandler and FileHandler has the attribute create, myfile inherently has that attribute and therefore we can call it as a method! Let's see what went on here.
Assuming that i am in the Documents folder this is what happened
- Before `myfile.Create()`
````yaml
- Documents
  - main.py
````
- After `myfile.Create()`
````yaml
- Documents
  - main.py
  - ThisThing.txt
````
This has happened because `myfile.Create()` uses the filename we've given it in the variable `File` as a string to create the file! Because in the source code it uses the `open()` built-in function so if the file isn't there, it is created, however if it is already there it will give you an error because you tried to create a file that already exists!

Following this, on the topic of the file existing, we can use the method `myfile.Exists()` to get a boolean (True or False) value returned to us based on whether or not the filename of the Path we've given it exists! We can even put it in an `if` statement (since it checks for a boolean value) to print out something special.
```python
if myfile.Exists():
  print("My file now exists!")
else:
  print("Somethign must've happened :(")
```

Now that we've created our file and we know that it exists, we can do some reading and writing to it from inside of the program. This can be good if we are wanting to for exampel create a mock Banking system perhaps or store data from a variable. For this we can use `myfile.Write(String="Hello World").
```python
myfile.Write("Hello World")
```
Now that we've written to the file, if you wanted to make sure that the string is in there, we could do one of two things. We could either open up the text file to see for ourself or we could use another method of FileHandler called `Read()`.
```python
WhatsInourFile = myfile.Read(ReturnType=str)
print(WhatsInourFile)
```
In the `Read()` method, i have specified an argument called `ReturnType`. As of v0.13, QEtils doesn't have ReturnType with a default value and so we must tell it what type of value we want it to give us.

Now that we've done all we can with our file, we can remove it because we no longer need it for this example, let's call the following method

```python
myfile.Delete()
```

Once you're finished, you can have a play around with what you know already and then you might have some code that looks a little like this
```python
from QEtils import FileHandler as FH #Import the FileHandler

MyFile = FH(File=input("What would you like your file to be called?")) #Create an instance

[MyFile.Write(input("Let's add something to that file!"), Suffix="\n") for x in range(9)] #Ask for 10 things to add to the file

for index, EachLine in enumerate(MyFile.Read(ReturnType=list, Separator="\n")): #Loop each item in the list returned by Read
  print(f"Line {index} says: '{EachLine}'") #Print it out with an f string
  
MyFile.Delete() #We've had our fun and no longer need the file so we can remove it
```
---
## FileHandler

### `FileHandler(File="Temp.tmp", Path="Files/Temps/")`
- Takes 2 arguments
  - File: This argument takes a string which is to be the name of the actual file that is to be opened, No default value
  - Path: This arguments takes a string which is to be the path in which the file is to be Created/Edited/Deleted etc, Default value is `""`, ignored for directory of file which is being run
- Creates an instance of the FileHandler class with the correct attributes

### `Create()`
- Takes no arguments
- Creates the file if following condition/s are met
  - The file does not already exist
  - The file path is able to be created
  
### `Delete()`
- Takes no arguments
- Deletes the file if following condition/s are met
  - The file already exists
  - The path to the file is valid
  
### `Write(String="2 String", Prefix="1 String ", Suffix=" 3 String", Overwrite=True)`
- Takes 4 arguments
  - String: This argument takes a string and allows you to set the middle string that will be written to the file, No default value
  - Prefix: This argument takes a string and allows you to set the left most string that will be written to the file, No default value
  - Suffix: This argument takes a string and  allows you to set the right most string that will be written to the filem Default value is `\n`
  - OverWrite: This argument takes a boolean and allows you to tell the method whether or not to overwrite any existing text in the file, Default value is `False`
- Writes the 3 former arguments to the file, using the `OverWrite` variable to decide whether or not to remove everything from the file first
  
### `Read(ReturnType=dict, Separator="\n", Discriminator="LineOfIndex")`
- Takes 3 arguments
  - ReturnType: This argument takes a type from `[str, list, dict]` and allows you to choose what type of return value the method will have, Default value is `str`
  - Separator: This argument takes a string and allows you to choose for both the `dict` and `list` types what will be used to separate them into their iterable forms, Default value is `""`, ignored
  - Discriminator: This argument takes a string and allows you to choose what the prefix will be for the `dict` type return value, Default value is `""`, ignored
- Returns a variable of type based on the ReturnType wanted using the `Separator` and `Discriminator` variables as explained above 