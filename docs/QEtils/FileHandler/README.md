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
```yaml
- Documents
  - main.py
```
- After `myfile.Create()`
```yaml
- Documents
  - main.py
  - ThisThing.txt
```
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
## FileHandlerClass

### `Create()`

### `Delete()`

### `Write(String="2 String", Prefix="1 String ", Suffix=" 3 String", Overwrite=True)`

### `Read(ReturnType=dict, Separator="\n", Discriminator="LineOfIndex")`
