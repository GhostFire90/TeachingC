Functions, similar to loops, is a way to repeat the same section of code, however unlike loops functions are intended to be used for different purposes based on the *arguments* passed in

Lets break down one that we are somewhat familiar with, [the main function](<./../Explanations/Main Function.md>)
```c
int main(void){

}
```

so what does it mean? Similar to [variables](<./Variables.md>)  it starts with a [return](#Return) type, then the name of the function, but what's `(void)` mean? So the main function in this context is a special case, but essentially what you put in there follows the same convention as creating a variable, and essentially works like that as well. Lets look at a more standard function declaration

```c
int foo(int bar){
	// doesnt do anything yet!
}
```

This is a function called `foo` that takes in any integer and sets the local variable bar (explained in [Scopes](<./Scopes.md>)) to whatever value is passed to it, lets add some functionality then!

```c
int foo(int bar){
	printf("Bar = %d\n", bar);
}
```

now whatever number you call foo with, will get printed like so
```c
foo(5);
// Bar = 5
foo(42);
// Bar = 42
// etc...
```

So what if we want the function to calculate something and give the calculated value back?

## Return

Say you want a function to take a number $n$ and square it ($n*n$), this is obviously easy but putting $n*n$ all over your code can make it look messy and hard to read, so lets create a function for it!
```c
int square(int n){
	// what to do here?
}
```
sure we can just put $n*n$ but then what? that wont give us any value back as n is a copy of whatever is passed in (Deeper explanation in [Pointers](<./Pointers.md>)), this is where the `return` statement comes in. As I mentioned previously the type-name is called the *return type* this tells the user (and the compiler) what is expected for the function to give back, in this case an `int`
```c
// n is an integer, so squaring it should result in an int, so the return type is int
int square(int n){
	return (n*n); // Whatever is placed after the return is the value returned
}
```

Return statements have a special use as well, similar to [break](<./Loops.md#Break>), wherever it is called, the function immediately ends. 

now instead of using $n*n$ in your code all over the place you can instead do 
```c
int a = square(n); // a is now the square of n
int b = square(5); // b is now the square of 5, so 25, etc
```

## What are Arguments/Parameters

Arguments aka Parameters for a function are what you place inside the parenthesis, whether calling or creating a function, there are two main differences however
```c
int foo(int a);
foo(a);
```
When creating a function you HAVE to specify the type vs when you call the function you don't. However if you try to call a function with the wrong argument type **YOUR PROGRAM WILL NOT COMPILE**

But arguments are essentially variables local ONLY to the function, and what gets passed in when they are called gets COPIED and the variable gets set to it, so 

```c
int foo(int a){
	a = 5; // local copy of a gets set to 5
	return 0;
}
int a = 0; // a is 0

foo(a); // call foo

printf("%d\n", a); // a is STILL 0 because it was a COPY

```

## Void functions

Sometimes you want a function to just DO something, you don't need data back or anything. These are called Void functions, Void will possibly get a whole topic of its own but for now all you need to know is it tells a function that it doesn't return anything.

```c
int foo(int a){
	printf("%d\n", a);
	return 0;
}

void foo(int a){
	printf("%d\n", a);
}
```
both of these functions do the same thing, however for the user of the function it is much easier to read the void one as they know NOT to expect anything from it

### Returns in void functions

Return in void acts the same way as previously, stopping the function, however you cannot supply a value to it

```c
void foo(int a){

	if(a > 5){
		return;
	}
	printf("%d", a);

}
foo(0);
foo(1);
foo(2);
foo(3);
foo(4);
foo(5);
```

<details><summary>What would this print?</summary>01234</details>

