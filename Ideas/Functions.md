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
sure we can just put $n*n$ but then what? that wont give us any value back as n is a copy of whatever is passed in (Deeper explanation in [Pointers](<./Pointers.md>)), this is where the `return` statement comes in. As I mentioned previously the type-name is called the *return typer* 

