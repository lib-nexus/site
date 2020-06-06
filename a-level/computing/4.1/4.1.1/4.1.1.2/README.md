## Topic Quota

> Use, understand and know how the following statement types can be combnied in programs
> * variable declaration
> * constant declaration
> * assignment
> * iteration
> * selection
> * subroutine ( procedure/function )
> Use definite and indefinite iteration including indefinite iteration with the condition/s at the start or the end of the iterative structure. A theoretical understanding of conditon/s at either end of an iterative structure is required, regardless of whether they are supported by the language being used
> Use nested selection and nested iteration structures
> Use meaningful identifier names and know why it is important to use them

## Statement types

In programming languages, all statements can be used in combination to create a functional program. However, the scope does matter when deciding how to use these in conjunction with one another. For example, the following static method written in typescript displays all of this properly in use

```ts
const AuthorName = "Quentin"; //Declare a constant ( unchangeable ) variable, doesn't need to be changed
var Pages = 1; //Declare a changeable variable, that could need to be changed

Pages = 2; //Assign the value of 2 to the Pages variable, because now there's two pages

for (var i = 0; i < AuthorName.length; i++) { console.log(AuthorName[i]); } //Definite ( Defined Iteration Length ) iteration of characters within AuthorName variable

if (Pages > 1) { console.log("We have more than one page!"); } //Selection using condition Pages being more than one two log that we have more than one page

function LongName(Name: string) { return Name.length > 10; } //A procedure we can use to return whether or not our name's length is greater than 10

i = 1
while (i != 4) { console.log(i); i = Math.floor(Math.random()*5); } //Indefinite ( Undefined Iteration Length ) iteration condition variable i not having an integer value of 4 

//At this point in check criteria, i deliberated between switching language to a password checker in c# i had already made but chose to stay with typescript, let's recreate it here

function PasswordSecure(Password: string)
    {
        var LowerCaseSymbols = "qwertyuiopasdfghjklzxcvbnm"; //Define lower case symbols
        var UpperCaseSymbols = "QWERTYUIOPASDFGHJKLZXCVBNM"; //Define upper case symbols
        var SpecialSymbols = "!\"£$%^&*()_+-=[]{};'#:@~,./<>?\|"; //Define special symbols
        var NumberSymbols = "1234567890"; //Define number symbols
        var LowerCaseInString, UpperCaseInString, SpecialInString, NumberInString; //Declare variables to be used later on
        LowerCaseInString = UpperCaseInString = SpecialInString = NumberInString = 0; //Set them all to the same amount after declaration

        for ( var i = 0; i < Password.length; i++ ) //Iterate through each character of the Password string
        {
            for ( var y = 0; i < LowerCaseSymbols.length; i++ ) { if (LowerCaseSymbols.includes(Password[i]) ) {LowerCaseInString++} } //Iterate through each character of the LowerCaseSymbols string to see if current password char is in that string, if so, increment respectively
            for ( var y = 0; i < UpperCaseSymbols.length; i++ ) { if (UpperCaseSymbols.includes(Password[i]) ) {UpperCaseInString++} } //Iterate through each character of the UpperCaseSymbols string to see if current password char is in that string, if so, increment respectively
            for ( var y = 0; i < SpecialSymbols.length; i++ ) { if (SpecialSymbols.includes(Password[i]) ) {SpecialInString++} } //Iterate through each character of the SpecialSymbols string to see if current password char is in that string, if so, increment respectively
            for ( var y = 0; i < NumberSymbols.length; i++ ) { if (NumberSymbols.includes(Password[i]) ) {NumberInString++} } //Iterate through each character of the NumberSymbols string to see if current password char is in that string, if so, increment respectively
        }

        if ( LowerCaseInString <= 2 && UpperCaseInString <= 2 && SpecialInString <= 2 && NumberInString <= 2 && Password.length > 10 ) { return true; } else { return false; } //Do a final check to make sure that they all meet a good password creating criteria
    }

// The above shows nested iteration as well as some other simple things

if ( Author == "Quentin" ) { if ( Pages > 1 ) { console.log("Quentin has made more than one page!") } } //Nested selection check for if both statements pass, this is very inefficient however and is why the AND ( && ) operator exists
```

For the final criterion for this topic, one must understand what meaningful identifier names are and why it is important to use them. In the above code snippet, you can see that i have named my variables dynamically, if you didn't know the value, you could probably guess what value they might have. This is what a meaningful identifier is. It is something that allows you to properly identify it from context. This is very important for example if you are debugging. You would much rather have the error say `'NumberOfBirthdays' variable is not of predicted type` than it say `'Variable1' variable is not of predicted type`. You can find it easier that way!