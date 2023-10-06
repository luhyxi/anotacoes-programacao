---
tags:
  - projects
Area: "[[!C-Sharp]]"
Status: In progress
topic:
---
# Dia 04/10:


# Dia 05/10:
### Try Catch:

1. In C#, the `try-catch` block is a fundamental mechanism for handling exceptions, which are unexpected or erroneous situations that can occur during the execution of a program.

2. **Try Block**: The `try` block encloses the code that may potentially throw an exception. It's where you place the code that you want to monitor for exceptions.
```csharp
try
{
    // Code that may throw an exception
}

```

3. **Catch Block**: If an exception is thrown within the `try` block, the program immediately jumps to the corresponding `catch` block. The `catch` block is responsible for handling the exception. You can specify the type of exception you want to catch or catch a general `Exception` type to handle all exceptions.
```csharp
catch (ExceptionType ex)
{
    // Code to handle the exception
}

```

4. **Exception Handling**: Inside the `catch` block, you can write code to handle the exception gracefully. This can include logging the error, displaying a user-friendly message, or taking other appropriate actions to recover from the exception. 
```csharp
try
{
    int result = 10 / 0; // This will throw a DivideByZeroException
}
catch (DivideByZeroException ex)
{
    Console.WriteLine("An error occurred: " + ex.Message);
}


```

### CultureInfo:

**System.Globalization Namespace:** 
The `System.Globalization` namespace provides classes and enumerations for working with culture-specific information, such as date and time formatting, number formatting, and string comparison. It allows you to adapt your applications to different cultures and regions, ensuring that they can display information in a way that is familiar and meaningful to users from various parts of the world.

**Exemples:**
1. **CultureInfo**: This is one of the central classes in this namespace. It represents a specific culture or region and provides information about that culture, such as its language, calendar system, date and time formatting, and number formatting rules.
    
2. **RegionInfo**: This class provides information about a specific geographic region, including its currency, time zones, and more.
    
3. **DateTimeFormatInfo**: It contains information about how dates and times are formatted in a specific culture, including date and time patterns, month and day names, and AM/PM symbols.
    
4. **NumberFormatInfo**: This class contains information about how numbers are formatted in a specific culture, including decimal and thousand separators, currency symbols, and more.

**Example:**
```csharp
using System;
using System.Globalization;

class Program
{
    static void Main()
    {
        // Create a CultureInfo for the French culture
        CultureInfo frenchCulture = new CultureInfo("fr-FR");

        // Format a date using French culture
        DateTime date = DateTime.Now;
        string formattedDate = date.ToString("d", frenchCulture);
        Console.WriteLine(formattedDate); // Output: 06/10/2023 (for French culture)

        // You can similarly use CultureInfo for number formatting and string comparisons.
    }
}
```

## FOCO EM INTERAÇÃO COM O CONSOLE!!
### String Concatenation:
In C#, there are several methods for concatenating strings, each with its own characteristics. Let's explore these methods:

1. **String Concatenation Operator `+`:**
   - **How it Operates:** The `+` operator is a simple and straightforward way to concatenate strings. It works by combining two or more strings into a single string.

   ```csharp
   string str1 = "Hello, ";
   string str2 = "world!";
   string result = str1 + str2; // Concatenates str1 and str2
   ```

2. **String Interpolation (with `$` symbol):**
   - **How it Operates:** String interpolation allows you to embed expressions or variables directly within a string by placing them within curly braces `{}`. The values of the expressions or variables are automatically inserted into the string.

   ```csharp
   string name = "Alice";
   int age = 30;
   string message = $"My name is {name} and I am {age} years old.";
   ```

3. **String.Concat Method:**
   - **How it Operates:** The `string.Concat` method concatenates one or more strings and returns a new string that contains the concatenated values.

   ```csharp
   string str1 = "Hello, ";
   string str2 = "world!";
   string result = string.Concat(str1, str2); // Concatenates str1 and str2
   ```

4. **String.Join Method:**
   - **How it Operates:** The `string.Join` method concatenates an array or collection of strings into a single string, separating them with a specified delimiter.

   ```csharp
   string[] words = { "Hello", "world", "in", "C#" };
   string result = string.Join(" ", words); // Concatenates words with spaces in between
   ```

5. **StringBuilder Class (FASTEST!!!):**
   - **How it Operates:** `StringBuilder` is a mutable class specifically designed for efficient string concatenation, especially when you need to perform many string concatenation operations in a loop. It avoids the performance overhead of repeatedly creating new strings.

   ```csharp
   StringBuilder sb = new StringBuilder();
   sb.Append("Hello, ");
   sb.Append("world!");
   string result = sb.ToString(); // Converts StringBuilder to a string
   ```

   The `StringBuilder` class provides methods like `Append`, `AppendLine`, and `Insert` to build strings efficiently.
### StringBuilder Exemples:

1. **Appending Text in a Loop:**
   You can efficiently build a string by repeatedly appending text in a loop, such as when constructing a long piece of text or generating CSV data.

   ```csharp
   StringBuilder sb = new StringBuilder();
   for (int i = 1; i <= 10; i++)
   {
       sb.Append($"Item {i},");
   }
   string result = sb.ToString();
   // Result will be: "Item 1,Item 2,Item 3,Item 4,Item 5,Item 6,Item 7,Item 8,Item 9,Item 10,"
   ```

2. **Inserting Text at Specific Positions:**
   You can use the `Insert` method to insert text at specific positions within a `StringBuilder`.

   ```csharp
   StringBuilder sb = new StringBuilder("Hello, world!");
   sb.Insert(6, "beautiful ");
   string result = sb.ToString();
   // Result will be: "Hello, beautiful world!"
   ```

3. **Appending Lines with `AppendLine`:**
   `AppendLine` appends a string followed by a line terminator (usually `\r\n` on Windows) to the `StringBuilder`, which is useful when building multi-line text.

   ```csharp
   StringBuilder sb = new StringBuilder();
   sb.AppendLine("Line 1");
   sb.AppendLine("Line 2");
   string result = sb.ToString();
   // Result will be:
   // "Line 1\r\n"
   // "Line 2\r\n"
   ```

4. **Clearing the StringBuilder:**
   You can use the `Clear` method to remove all content from the `StringBuilder`.

   ```csharp
   StringBuilder sb = new StringBuilder("Some text");
   sb.Clear(); // Clears the content
   ```

5. **Setting Capacity:**
   You can set the initial capacity of the `StringBuilder` to optimize performance if you have an idea of how large the final string will be.

   ```csharp
   StringBuilder sb = new StringBuilder(100); // Initial capacity of 100 characters
   ```

6. **Replacing Text:**
   You can replace text within a `StringBuilder` using the `Replace` method.

   ```csharp
   StringBuilder sb = new StringBuilder("Hello, world!");
   sb.Replace("world", "C#");
   string result = sb.ToString();
   // Result will be: "Hello, C#!"
   ```

7. **Appending Formatted Text:**
   You can use the `AppendFormat` method to append formatted text, similar to how you use `string.Format`.

   ```csharp
   StringBuilder sb = new StringBuilder();
   sb.AppendFormat("Name: {0}, Age: {1}", "Alice", 30);
   string result = sb.ToString();
   // Result will be: "Name: Alice, Age: 30"
   ```

8. **Chaining StringBuilder Methods:**
   You can chain multiple `Append` and `AppendLine` methods together to build complex strings efficiently.

   ```csharp
   StringBuilder sb = new StringBuilder();
   sb.Append("Hello")
     .Append(", ")
     .Append("world!")
     .AppendLine()
     .Append("Have a nice day.");
   string result = sb.ToString();
   // Result will be:
   // "Hello, world!"
   // "Have a nice day."
   ```

`StringBuilder` is a versatile class for efficiently manipulating strings, especially when you need to perform multiple string concatenation operations in a memory-efficient way.

### Regex:
**Definition:** Regex (regular expressions) is a set of patterns that get regular expressons and match, search for and manipulate a set of strings to that pattern.
1. **Creating a Pattern -** Regex consist of a combination of characters and metacharacters that have special meanings - **Examples**: 
	`\d{2} 9\d{4}-\d{4}` Formato para numeros de celulares BR
	`\d{3}-\d{2}-\d{4}` Social Security Number (SSN)
2. **Using the Regex Class:** 
	In C#, you can work with regular expressions using the `System.Text.RegularExpressions.Regex` class. You typically create an instance of this class with your regular expression pattern
	
 ```csharp
using System;
using System.Text.RegularExpressions;

class Program
{
    static void Main()
    {
        string input = "My SSN is 123-45-6789.";
        string pattern = @"\d{3}-\d{2}-\d{4}";
        Regex regex = new Regex(pattern);
    }
}
 ```

3. **Matching Text:** 
	Once you have a `Regex` instance, you can use its methods to search for and match text in a given input string. The most common methods are:
- `Match`: This method searches for the first occurrence of the pattern in the input string and returns a `Match` object with information about the match.   
- `Matches`: This method finds all occurrences of the pattern in the input string and returns a collection of `Match` objects.
```csharp
Match match = regex.Match(input); 
if (match.Success) 
{     
Console.WriteLine("Found SSN: " + match.Value);
}
```

4. **Accessing Match Information:**
	The `Match` object contains information about the matched text, including the text itself, the starting position, and the length of the match. You can access this information using properties like `Value`, `Index`, and `Length`.

5. **Replacing Text:** 
	Regex can be used to replace parts of a string that match a pattern with another string. You can use the `Regex.Replace` method for this purpose.
```csharp
string newInput = regex.Replace(input, "XXX-XX-XXXX");
Console.WriteLine("Updated input: " + newInput);
```

### Ternary:
In C#, a ternary operator is a concise way to write a conditional expression. It allows you to assign a value to a variable based on a condition. The ternary operator is often used as a shorthand for simple if-else statements. Here's how it works:

The basic syntax of the ternary operator is as follows:

```csharp
variable = (condition) ? expression_if_true : expression_if_false;
```

- `condition`: A Boolean expression that evaluates to either `true` or `false`.
- `expression_if_true`: The value to assign to the variable if the condition is `true`.
- `expression_if_false`: The value to assign to the variable if the condition is `false`.

Here's an example of using the ternary operator to assign a value to a variable based on a condition:

```csharp
int age = 20;
string message = (age >= 18) ? "You are an adult" : "You are a minor";
```

In this example, the condition `(age >= 18)` is evaluated. If it's `true` (in this case, because `age` is 20), the variable `message` will be assigned the string `"You are an adult"`. If it's `false`, it will be assigned the string `"You are a minor"`.

The ternary operator can be used for any data type, not just strings. Here's an example using it for numeric values:

```csharp
int x = 10;
int y = 5;
int result = (x > y) ? x : y; // result will be 10
```

In this case, if `x` is greater than `y`, `result` will be assigned the value of `x`, which is 10. Otherwise, it will be assigned the value of `y`, which is 5.

Ternary operators are handy for simple conditional assignments and can make your code more concise and readable. However, for more complex conditions or multiple possible outcomes, it's often better to use traditional if-else statements for clarity.

Q1: Can you provide an example of using a ternary operator in C# for a scenario other than assigning values to variables?
Q2: Are there any limitations or considerations to keep in mind when using ternary operators in C#?