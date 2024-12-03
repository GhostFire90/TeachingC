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
Type in c: `float`, `double`
What it stores: Any number, can also contain decimals

### Character 
Type in c: `char`
What it stores: a character but it also doubles as an integer that can only store 0-255

### Pointer
Type in c: any type-name followed by a `*`
Explanation is in the [Pointer](<./Pointers.md>) page as they are quite complicated

## Modifiers

### Unsigned
By default integers are *signed* which means they can be either positive or negative, unsigned makes it so they can only be positive, however this comes with some other complications that will be covered in [binary](<./../Theory/Binary.md>)
#### Ex:
`unsigned char`
`unsigned int`
`unsigned` (this one is equivalent to `unsigned int`)

### Short/Long
Sometimes, we need a bigger number to fit into a variable, due to limitations (also explained in [binary](<./../Theory/Binary.md>)) default we cant use the default size. This is a double sided problem, what if we need to use as little memory as possible and we know our max for a variable is smaller than the default? This is where short and long come in. 

#### Short
Short is usually used by itself but can also be used with `int` or `unsigned` or any combo of the two, basically it is half the default size of `int`

#### Long
Long is more of the same but its double the default size of int

#### Ex
`short int` == `short`
`long int` == `long`
`unsigned short`
`unsigned long`

## Pseudo types

These are types that *technically* don't exist, but C is implemented in a way where they are still available

### Boolean
What is it: Usually represents true or false
What is it in C: Any value that **IS NOT** equal to 0, is true, and 0 is false
Use case: used primarily in if statements, while, and for loops

### Strings
What is it: text that is made up of more than 1 character
What is it in C: `char*` usually, also commonly `const char*` 
[Strings](<./Strings.md>) have their own page that will cover more about the specifics of strings
What does the `*` symbol mean? That marks a variable as a Pointer, we will cover that in the later [Pointer](<./Pointers.md>) page



