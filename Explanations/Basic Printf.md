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
| s | 