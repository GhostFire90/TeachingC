Pointers in all technicality are their own type. Think of them like your home address sort of thing, to tell someone where you live, you give them the address to your house.

All a pointer is, is an address to where some chunk of data lives, it is declared like so

```c
<typename>* varname;
```
the star is important, that is how you know its a pointer.
```c
int* i;
```
that basically means "i is an address that *points* to where an integer lives" 

## What can we do with this?

say you want a function that squares a number that it is given

```c
void square(int i){
 i *= i;
}

int main (void){
	int i = 2;
	printf("i before square %d\n", i);
	square(i);
	printf("i after square %d\n", i);
}
```

this unfortunately prints :
> i before square 2
> i after square 2

this is due to how parameters are *copies* like mentioned in [Functions](<./Functions.md>), this of course can be fixed with return values, however in certain scenarios like wanting multiple values back from a function or [Structs](<./Structs.md>), return values simply arent enough.

So lets fix this function using pointers

```c
// Square is a *function* that takes a *pointer* to an integer
void square(int* pi){
 *pi *= *pi;
}

int main (void){
	int i = 2;
	printf("i before square %d\n", i);
	square(&i);
	printf("i after square %d\n", i);
}
```

Now what is that `&` sign for? So far we have only covered what pointers ARE, not how to get them. There are two core ways to get a pointer:
1. the `&` symbol says "Give me the address (pointer) of this variable" 
2. [Dynamic Memory](<./DynamicMemory.md) 
And what's the `*i` mean? That is called *dereferencing* a pointer, basically what it does is says "Go to that address and tell me/change whats there" so `*i *= *i` reads like: "Multiply the *value* at the address `pi` by the *value* at the address `pi`" this will effectively change the value of i to its square.


