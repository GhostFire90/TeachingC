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

this is due to how parameters are *copies* like mentioned in []