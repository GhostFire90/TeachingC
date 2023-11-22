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

another valid example:
```c
#include <stdio.h> // for printf
int main(void){
	int i; //create i;
	for(i = 0; i < 10; i++){
		printf("Hello");
	}	
}

```
This works because you dont need to create the variable in the for loop, there are some other shenanigans that will be explained in [Extended Loops](</Ideas/Extended Loops.md>)

### Use cases
- When you know the code you're running needs to run $n$ times
- Moving through an [Array](/Ideas/Arrays.md)

## While Loops
So what if you *don't* know when a loop should end? Like waiting on a user to enter a certain input
```c
#include <stdio.h> // for printf

int main(void){
	char c = 'A'; // Since we havent covered user input yet, this is a placeholder value
	while(c != 'B'){
		printf("%c", c);
		// Get user input here!
	}
}

```

This reads like "While c is *not* contain the value 'B' keep printing c and getting new user input"

Maybe you want a loop to never end? (very slim use cases)
```c
int main(void){
	while(1){
		//do stuff here
	}
}
```
Since as we covered in [Variables](/Ideas/Variables.md#Boolean), any value that *isn't* 0, is considered true, the condition will always be true

### Use Cases
- When you're not sure how many times a loop needs to run
- Infinite loops

## Continue and Break

Sometimes in loops, you want to skip an entry or maybe stop the loop early all together. In c, this is as easy as either using `continue` or `break` 


### Continue
```c

for(int i = 0; i < 10; i++){
	if(i == 5){
		continue;
	}
	// do something
}

```
This code is very simple, basically it reads as "do something"