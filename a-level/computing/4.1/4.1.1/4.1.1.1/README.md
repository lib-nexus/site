## Topic Quota

> Understand and Use the following appropriately
> * integer
> * real/float
> * noolean
> * character
> * string
> * date/time
> * pointer/reference
> * records ( or equivalent )
> * arrays ( or equivalent )
> Define and use user-define data types based on language-defined ( built-in ) data types

## Data Types

| Data Type | Description | Example 1 | Example 2 | Alias/es |
| --- | --- | -- | --- | --- |
| Integer | A whole positive or negative number | 1  2 | int |
| Float | A non whole positive or negative number ( has decimal place ) | `3.14` | `0.69` | real/double |
| Boolean | An expression that results in something being true or false | `1 == 2` | `false` | bool/boolean |
| Character | A single character from the ascii table of characters | `a` | `b` | char |
| String | A string of characters aka a character array | `Quentin` | `Rick Astley` | str/string |
| Datetime | A structure to contain a date and time in a lang define format, commonly `YYYY-MM-DD hh:mm:ss[.nnn]` | `2004-03-13 08:30:00` | `2020-06-06 04:03:00` | datetime |
| Pointer | The address where data is stored ( the variable ) as opposed to the data itself | `0x12938193` | `0x19238123` | pointer/reference |
| Dictionary | A data type that stores information data in a formatted data structure | `{ "Q" : { "Programmer": True, "Sixth Former": True } }` | `{ "ResponseType": "Success" }` | record/dict/hash |
| Array | A data type that stores information in a structure, languages like Java, C# and C++ require these arrays to be typed | `["Beep Beep", "I'm a sheep"]` | `{'a', 'b', 'c'}` | array/list |
| User defined Data Type | These are data structures that categorise information mostly based on lang defined data types | `class StaticStruct { public static string AString { get; set; } } | class/struct/interface |

### How a pointer works

A pointer is something that stores that address of a variable for later reference. For example

```java
int x1, x2, x3;
x1 = x2 = x3 = 0;

System.out.println(x1, x2, x3);
```

That would mean that there needs to be pointers leading to variables of x1, x2, and x3 in order for them to be able to be referenced

## How a user defined data type works

A user defined data type is a way of categorising information based on a user defined structure, this mostly is based on pre-existing data types like the below examples for a human data type

#### Java - Class

```java
public class Human
{
    private String Name;
    private int Age;
    private double Height;

    public Human(String Name, int Age, double Height)
    {
        this.Name = Name;
        this.Age = Age;
        this.Height = Height;
    }
}
```

#### C# - Class

```cs
public class Human
{
    private string Name;
    private int Age;
    private float Height;

    public Human(string Name, int Age, float Height)
    {
        this.Name = Name;
        this.Age = Age;
        this.Height = Height;
    }
}
```

#### Python - Class

```python
class Human:

    def __init__(self, Name: str, Age: int, Height: float): 

        self.Name = Name
        self.Age = Age
        self.Height = Height
```

#### Go - Struct

```go
struct Human() {
    Name   string
    Age    int
    Height float64
}
```

#### JavaScript - Interface

```javascript
class Human {
    Name: string;
    Age: int;
    Height: float;
}
```