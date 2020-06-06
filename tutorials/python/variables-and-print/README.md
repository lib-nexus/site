## [Home](http://libnexus.github.io/Site) | [Docs](https://libnexus.github.io/Site/docs) | [Blog](https://www.youtube.com/watch?v=dQw4w9WgXcQ) | [Tutorials](https://libnexus.github.io/Site/tutorials) | [A-Level](https://libnexus.github.io/Site/a-level) | [Contact](https://libnexus.github.io/Site/contact) | [Résumé](https://libnexus.github.io/Site/résumé)

## Variables and Print tutorial

If you're on this page it's likely that you are either a beginner to programming, you have forgotten how to do somethings over time or you want to learn python. Python is an `Object Oriented Programming` language which means that it mostly is comprised of things called `objects`. We can assign these objects to things called `variables` which allow us to easily store and recall information. 

Let's take a look at some simple programming code which you should be able to understand properly and fully by the time this tutorial is over.

```python
1. MyName = "Q"
2. print("Hello World")
3. print("I was created by " + MyName)
```
Here we can see that there are 3 lines of code. 
- On the first line we have a variable that is assigned to an instance (object) of the `string` class which we can just call a 'string'. 
- On the second line we are printing a 'string' by itself. 
- On the third and last line we are printing the string 'I was created by ' as well as the variable that we assigned a `string` value to, so we can call it a 'string'. 

This first line tells python that when we say `MyName` we want the string value `Q`. This is quite like real life. If someone were to ask me for my name, i wouldn't say `name` i would say `Q`. 

The second line tells python that we want to `print` to the console, everything inside of the brackets. In this case we are telling it that we want to print a string value of `Hello World`.

Finally, the last line tells python that just like the above line, we want to print everything in the brackets however this time we have done something called `concatenation`. This `concatenation` is the equivalent to putting to string together. Once again, this is quite like real life. If someone were to ask me for my name and age, i would say `Q, 16`. However, don't forget that python is a programming language so it only does what we tell it to do. Therefore the above syntax isn't appropriated by python. therefore, it prints exactly `I was created by Q`.

Using this knowledge, create a pyhon program that says `Hello World` on one line and then on the next says `I was created by YOURNAME` where YOURNAME is your name.

## Variable data types

In other languages you may have come across, you might have seen that a variable normally has it's type declared when it's about to be used. However, python uses `implicit` typing which means the type of object that you put on the other side of the 