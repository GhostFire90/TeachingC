## Definition 
A Variable in C is anything that stores a value, whether its a number, some text, a single letter, or a decimal number (they are different sadly)

Some example definitions
```c
int i = 0;

float f = 0.0f;

char c = 'A';
char* str = "Hello World";

```

there are a lot of new words and symbols in that block of code so let me break down a variable declaration in some more complex terms
```c
//int is the type of data the variable stores, in this case it stands for integer
//i is the name of the variable
// = 0 is optional most of the time®, but in this case it sets the variable to 0 immediately
int i = 0;
```
so the way you declare a variable goes like this
```c
//int       i
<var type> <var name>;
```
## Types

### Integer
Type in c: `int`
What it stores: Any number that doesn't contain decimal points

### Float
Type in c: `float`
What it stores: Any number, can also contain decimals

### Character 
Type in c: `char`
What it stores: a character but it also doubles as an integer that can only store 0-255

## Pseudo types

These are types that *technically* don't exist, but C is implemented in a way where they are still available

### Boolean
What is it: Usually represents true or false
What is it in C: Any value that **IS NOT** equal to 0, is true, and 0 is false
Use case: used primarily in if statements, while and for loops

### Strings
What is it: text that is made up of more than 1 character
What is it in C: `char*` usually, also commonly `const char*` 
S



