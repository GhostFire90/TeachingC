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
for loops have 3 main parts, variable initialization where you set a variable to the starting number, conditional where you check if the condition is still true, and the increment. Each part has to be followed by a semi-colon `;`

```c
#include <stdio.h> // for printf

int main(void){
	// This reads like, Create variable i at the beginning, if i is less than 10, keep going, and at the end add 1 to it 
	for(int i = 0; i < 10; i++){
		printf("Hello");
	}
}
```

Lets break this down. `int i = 0` is the initialization this happens once, we create a new variable named i and set it to 0. 

`i < 10` this checks if i is still less than 10 this runs before the code every loop, if it is, it runs the code in the curly braces. 

Then finally `i++` This runs after the code in the curly braces gets run, basically what it means is after the code runs, add 1 to i.

### Pros
For-loops are mostly used for when you know when the loop needs to end, how many