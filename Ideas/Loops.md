Lets say you want to print the same thing over and over, say "Hello" 10 times
```c
#include <stdio.h> // for printf

int main(void){
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");
	printf("Hello");	
}
```
This is valid but is very crowded, this kind of problem is more fitting for a For loop since it is happening $n$ amount of times

## For Loop