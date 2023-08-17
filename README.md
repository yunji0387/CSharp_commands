# CSharp_commands

## Table of Contents
1. [How to create, build & run c#](#how_to_run)
2. [Object type](#object_type)
3. [Console functions](#console_functions)
4. [string functions](#string_functions)
5. [Number type functions](#number_functions)

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
