`printf` is one of the most important functions included in C. Its, as it is named, prints stuff to the screen.
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

below is a table of type specifiers

| Letter | Meaning |
| --- | --- |
| i | Integer Value |
| d | Integer value, outputted in decimal |
| x | Integer value, outputted in hex |
| c | Character value, outputted in ascii |
| s | const char* value, outputs a nul-terminated [String](<./../Ideas/String.md>) |
| p | [Pointer](<./../Ideas/Pointers.md), outputs the address |
| f | Floating point value (double OR float) |

However thats not all the format specifier can do. 
Lets say you wanted a specific number of characters taken up by your print?
say like
```
       100
```
where the total number of characters printed is 10, 7 spaces and 3 digits
if you put any number in FRONT of the type specifier, that will be the *minimum* of characters printed

```c
printf("%10d", 100);
```
