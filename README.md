# CSharp_commands

## Object type
- int (4 bytes : -2,147,483,648 to 2,147,483,647)
- long (8 bytes : -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
- float (4 bytes : 6 to 7 decimal digits)
- double (8 bytes : 15 decimal digits)
- bool (1 bit : true/false)
- char (2 bytes : character/letter)
- string (2 bytes per character)
- var (implicitly typed local variable - Must be initialize)

## Console functions
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
## string functions
### escape sequences
- ```c#
    Console.WriteLine("Hello\nWorld!"); // add new line
    Console.WriteLine("Hello\tWorld!"); // add tab
    Console.WriteLine("Hello \"World\"!"); // add "
    Console.WriteLine("c:\\source\\repos"); // add \
    Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)"); // @ keep all whitespace and character without need of escape backslash
    Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!"); // unicode escape character
  ```

## Number type
### integer
- 
