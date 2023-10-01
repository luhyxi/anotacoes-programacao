---
tags:
  - tech
  - MOCs
Area: "[[Programing]]"
---

---
# Planning
## Objectives:
- 


## Goals:
- 
- 
- 

# Definition:


# Technologies:



# Notes:
### Basics:

##### var declaration :
	type | name | value
	ex: string hello = "hi mom!";
##### null val :
	type(?) hello = null;
##### namespace -> use of class in other file
##### class:
	constructor -> public | name
	Destructor -> ~ | name
##### class obj:
	public | type | name
	{get;set;} -> redable and writable

##### Labdas:
	Func<param, param> name  = var =>

##### Async:
	async | type | name() {
		var name = await ...
		var name = await ...
		var name = await ...
	}


### Classes:

#### Classes in C (VIA CHAT GPT!!!)# 
are fundamental building blocks of object-oriented programming (OOP). They serve as blueprints or templates for creating objects, which are instances of a class. Classes encapsulate data (attributes) and behavior (methods) into a single unit. Here's a beginner-friendly explanation:
###### Blueprint for Objects: 
Imagine a class as a blueprint for creating objects. For example, if you're building a house, the blueprint specifies how the house should be constructed. In the same way, a class defines the structure and behavior of objects.
###### Attributes (Fields/Properties): 
A class can have attributes, also known as fields or properties, which represent data associated with the objects created from that class. These attributes define the characteristics or state of the objects. For instance, a Person class might have attributes like Name, Age, and Address.
###### Methods (Functions):
In addition to attributes, classes can contain methods, which are functions that define the behavior of the objects. These methods can perform actions or provide functionality related to the class. For example, a Car class might have methods like StartEngine(), Accelerate(), and Brake().
###### Encapsulation: 
One of the key principles of OOP is encapsulation. It means that a class hides its internal details from the outside world, and you can only interact with the class through its defined methods and properties. This helps in maintaining the integrity of the data and controlling how it's accessed and modified.

**How do Declare Classes:**

``` csharp
public class Person
{
    // Attributes (fields)
    public string Name;
    public int Age;

    // Methods
    public void Greet()
    {
        Console.WriteLine($"Hello, my name is {Name} and I am {Age} years old.");
    }
}
```

**Calling Classes:**
```csharp
// Create a Person object
Person person1 = new Person();
person1.Name = "John";
person1.Age = 30;

// Call a method on the object
person1.Greet(); // Output: "Hello, my name is John and I am 30 years old."


```

## [[Strings]] in C-Sharp

In C#, strings are not just arrays; they are sequences of characters represented as an array of characters (`char[]`). However, C# provides a higher-level abstraction for strings, making them easier to work with compared to traditional character arrays.

Here are some key points regarding strings in C#:

1. **Strings are Immutable:** One significant difference between strings and character arrays is that strings are immutable, meaning their content cannot be modified once they are created. When you perform operations on strings, you are actually creating new string instances.

2. **Indexing with `[ ]`:** You can use square brackets `[ ]` to access individual characters in a string. The index represents the position of the character in the string, starting at 0 for the first character.

   ```csharp
   string text = "Hello";
   char firstChar = text[0]; // Accesses the 'H' character
   ```

3. **Length Property:** You can get the length (number of characters) of a string using the `Length` property:

   ```csharp
   string text = "Hello";
   int length = text.Length; // length is 5
   ```

4. **String Methods:** C# provides a wide range of string methods for performing operations like substring extraction, concatenation, searching, and more. These methods make it convenient to work with strings without manually manipulating character arrays.

   ```csharp
   string text = "Hello, world!";
   string substring = text.Substring(0, 5); // "Hello"
   ```

5. **String Interpolation:** C# supports string interpolation, which allows you to embed expressions and variables directly within string literals using the `$` symbol.

   ```csharp
   string name = "Alice";
   int age = 30;
   string message = $"Hello, my name is {name} and I am {age} years old.";
   ```

In summary, while strings in C# are implemented as character arrays under the hood, they come with a set of convenient methods and abstractions that make working with text much more straightforward than directly manipulating character arrays. The `[ ]` indexing allows you to access individual characters by their position in the string.

Q1: Is there a specific task or operation you'd like to perform with strings or characters in C#?
Q2: Do you have any further questions about working with strings or arrays in C#?
Q3: Is there another topic or programming concept you'd like to explore?

# Commands

dotnet run -> RUN THE FUCKING CODE

---
### Sources: 

### Related Resources: 
```dataview
list
from [[]] and #tech 

```

