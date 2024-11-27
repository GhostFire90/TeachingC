`printf` is one of the most important functions included in C. Its, as it is named, prints stuff to the screen. `#include <stdio.h>` is *required* before your main function, we will cover what this does and why in [Includes](<./../Ideas/Includes.md>)

```c
int main(void){
	printf("Hello World!");
}
```
This simply prints "Hello World!" to the screen, however `printf` has more uses than that.

# Variable output

So what if we have a variable `int a = 5` and we want to print it to screen?
```c
printf("a");
```
that doesn't work, that'd only print the letter 'a' to screen, not the value of the variable.
```c
printf(a);
```
this doesnt work either since the first argument of `printf` has to be a `const char*` aka a c-string

# Format Specifiers

Format specifiers is how we solve this, the most simple format specifiers consist of a `%` and a type
```c
printf("%i", a);
```
`%i` in this context stands for Integer, what it outputs isn't standardized and can output the number in any format, so it is recommended to use `%d` instead, which stands for *decimal*
```c
printf("%d", a);
```
the string in the quotes is the only *required* argument for printf, it is called the **Format String**

below is a table of type specifiers

| Letter | Meaning |
| --- | --- |
| i | Integer Value |
| d | Integer value, outputted in decimal |
| x | Integer value, outputted in hex |
| c | Character value, outputted in ascii |
| s | const char* value, outputs a nul-terminated [String](<./../Ideas/Strings.md>) |
| p | [Pointer](<./../Ideas/Pointers.md>), outputs the address |
| f | Floating point value (double OR float) |

However thats not all the format specifier can do. 
Lets say you wanted a specific number of characters taken up by your print?
say like
```
       100
```
where the total number of characters printed is 10, 7 spaces and 3 digits
if you put any number, this is called the *width*, in FRONT of the type specifier, that will be the *minimum* of characters printed

```c
printf("%10d", 100);
```
what if you want it to be padded by 0's? like so
```
0000000100
```
so instead of spaces you want to fill it with zeros (note this only works with zeros), you put a 0 before the width. 
```c
printf("%010d", 100);
```

You can do similar with how many digits of precision (how many decimal places) in a floating point number to print (default is 6)
```
1.1111111111
```
that is 10 digits after the decimal point, you would put a width specifier AFTER a decimal point
```c
printf("%.10f", 1.111111111111111f);
```

# Arguments

Up to this point we've only used 2 arguments for printf, however it can have anywhere from 0 to $\infty$ as long as there are enough specifiers for it, $n$ specifiers means $n+1$ arguments (+1 for the format string). The way it achieves this is called [Variadic Functions](<./../Ideas/Variadic Functions.md>) and are a complex topic that will be covered later.

## Extra info

To Create a new line put `\n` in the format string where you want to make a new line
