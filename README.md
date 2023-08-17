# CSharp_commands

## Table of Contents
1. [How to create, build & run c#](#how_to_run)
2. [Object type](#object_type)
3. [Console functions](#console_functions)
4. [string functions](#string_functions)
5. [Number type functions](#number_functions)
6. [Expression(boolean)](#expression)
7. [Array type](#array)
8. [Random library](#random)

<a id="how_to_run"></a>
## How to create, build & run c#
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

1. make sure to have .NET SDK install
   - visit this [link for more detail](https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/6-exercise-install-dotnet).
2. make sure to have c# extension install in vs code
   - visit this [link for more detail](https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/5-exercise-configure-visual-studio-code).
3. create c# project
   - in Terminal run:
   ```c#
   dotnet new console -o ./CsharpProjects/TestProject
   ```
4. build c# project
   - first make sure terminal path located in the project folder, then run:
   ```c#
   dotnet build
   ```
5. run c# project
   - first make sure terminal path located in the project folder and has done step 4, then run:
   ```c#
   dotnet run
   ```

<!-- /MarkdownTOC -->
</details>

<a id="object_type"></a>
## Object type
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
   
- **int** (4 bytes : -2,147,483,648 to 2,147,483,647)
- **long** (8 bytes : -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
- **float** (4 bytes : 6 to 7 decimal digits)
- **double** (8 bytes : 15 decimal digits)
- **bool** (1 bit : true/false)
- **char** (2 bytes : character/letter)
- **string** (2 bytes per character)
- **var** (implicitly typed local variable - Must be initialize)

### integral types
- signed integral types
  ```c#
   Console.WriteLine("Signed integral types:");
   Console.WriteLine($"sbyte  : {sbyte.MinValue} to {sbyte.MaxValue}");
   Console.WriteLine($"short  : {short.MinValue} to {short.MaxValue}");
   Console.WriteLine($"int    : {int.MinValue} to {int.MaxValue}");
   Console.WriteLine($"long   : {long.MinValue} to {long.MaxValue}");

   Console.WriteLine("");
   Console.WriteLine("Floating point types:");
   Console.WriteLine($"float  : {float.MinValue} to {float.MaxValue} (with ~6-9 digits of precision)");
   Console.WriteLine($"double : {double.MinValue} to {double.MaxValue} (with ~15-17 digits of precision)");
   Console.WriteLine($"decimal: {decimal.MinValue} to {decimal.MaxValue} (with 28-29 digits of precision)");
   ```
   ```
   Signed integral types:
   sbyte  : -128 to 127
   short  : -32768 to 32767
   int    : -2147483648 to 2147483647
   long   : -9223372036854775808 to 9223372036854775807

   Floating point types:
   float  : -3.402823E+38 to 3.402823E+38 (with ~6-9 digits of precision)
   double : -1.79769313486232E+308 to 1.79769313486232E+308 (with ~15-17 digits of precision)
   decimal: -79228162514264337593543950335 to 79228162514264337593543950335 (with 28-29 digits of precision)
   ```
- unsigned integral types
  ```c#
   Console.WriteLine("");
   Console.WriteLine("Unsigned integral types:");
   
   Console.WriteLine($"byte   : {byte.MinValue} to {byte.MaxValue}");
   Console.WriteLine($"ushort : {ushort.MinValue} to {ushort.MaxValue}");
   Console.WriteLine($"uint   : {uint.MinValue} to {uint.MaxValue}");
   Console.WriteLine($"ulong  : {ulong.MinValue} to {ulong.MaxValue}");
  ```
  ```output
   Unsigned integral types:
   byte   : 0 to 255
   ushort : 0 to 65535
   uint   : 0 to 4294967295
   ulong  : 0 to 18446744073709551615
  ```

<!-- /MarkdownTOC -->
</details>

<a id="console_functions"></a>
## Console functions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
 
- console print new line
  ```c#
    Console.WriteLine("Hello World!");
    Console.WriteLine('H');
    Console.WriteLine(123);
  ```
- console print
  ```c#
    Console.Write("Hello World!");
  ```
- other
  ```c#
    Console.WriteLine("Hello" + " " + "World!");
  ```

<!-- /MarkdownTOC -->
</details>

<a id="string_functions"></a>
## string functions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### escape sequences
- ```c#
    Console.WriteLine("Hello\nWorld!"); // add new line
    Console.WriteLine("Hello\tWorld!"); // add tab
    Console.WriteLine("Hello \"World\"!"); // add "
    Console.WriteLine("c:\\source\\repos"); // add \
    Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)"); // @(verbatim) keep all whitespace and character without need of escape backslash
    Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!"); // unicode escape character
  ```
### interpolation
- string interpolation
  ```c#
    string message = greeting + " " + firstName + "!";
    // is same as
    string message = $"{greeting} {firstName}!";
  ```
- string interpolation and verbatim
  ```c#
    string projectName = "First-Project";
    Console.WriteLine($@"C:\Output\{projectName}\Data");
  ```

### Contains function
- check if a string contains a substring
  ```c#
   string pangram = "The quick brown fox jumps over the lazy dog.";
   Console.WriteLine(pangram.Contains("fox")); // True
   Console.WriteLine(pangram.Contains("cow")); // False
  ```
<!-- /MarkdownTOC -->
</details>

<a id="number_functions"></a>
## Number type functions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
   
### integer
- math operations
  ```c#
   int sum = 7 + 5; // 12
   sum += 5; // 17
   sum ++; // 18
   sum --; // 17
   sum -= 5; // 12
   sum = sum + 10; // 22
   int difference = 7 - 5; // 2
   int product = 7 * 5; // 35
   int quotient = 7 / 5; // 1
  ```
- modulus
  ```c#
   int a = 200 % 5; // 0
   int b = 7 % 5; // 2
  ```
### decimal
- decimal quotient
  ```c#
    decimal decimalQuotient = 7.0m / 5; // 1.4
  ```
  
<!-- /MarkdownTOC -->
</details>

<a id="expression"></a>
## Expression(boolean)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
 
- basics
  ```c#
   Console.WriteLine("a" != "a"); // False
   Console.WriteLine("a" != "A"); // True
   Console.WriteLine(1 != 2); // True
   string myValue = "a";
   Console.WriteLine(myValue != "a"); // False
  ```
  ```c#
   Console.WriteLine(1 > 2); // False
   Console.WriteLine(1 < 2); // True
   Console.WriteLine(1 >= 1); // True
   Console.WriteLine(1 <= 1); // True
  ```
### Conditional operator
- ```c#
   <evaluate this condition> ? <if condition is true, return this value: <if condition is false, return this value>
  ```
- example
  ```c#
   int saleAmount = 1001;
   int discount = saleAmount > 1000 ? 100 : 50;
   Console.WriteLine($"Discount: {discount}"); // Discount: 100
  ```
  
<!-- /MarkdownTOC -->
</details>


<a id="array"></a>
## Array type
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- int array
  ```c#
   int[] array = new int[10];
  ```
 
<!-- /MarkdownTOC -->
</details>

<a id="random"></a>
## Random library
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

```c#
Random dice = new Random();
int roll = dice.Next(1, 7); // limit number from 1 - 6 ( [1, 7) )
int roll1 = dice.Next(); // limit number from 0 - 2,147,483,647(int max) ( [0, int max) )
int roll2 = dice.Next(101); // limit number from 0 - 100 ( [0, 101) )
int roll3 = dice.Next(50, 101); // limit number from 50 - 100 ( [50, 100) )

Console.WriteLine(roll);  // 5
Console.WriteLine($"First roll: {roll1}"); // 342585470
Console.WriteLine($"Second roll: {roll2}"); // 43 
Console.WriteLine($"Third roll: {roll3}"); // 89
```
 
<!-- /MarkdownTOC -->
</details>
