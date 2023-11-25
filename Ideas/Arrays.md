Arrays in C have some funky ties to [Pointers](<./Pointers.md>) so this will be more of a general overview of arrays

## What are they
Arrays are most commonly, a collection of [variables](<./Variables.md>) of the same type. so instead of having

```c
int a;
int b;
int c;
int d;
```

we could have an array of integers that is 4 big
```c
int array[4];
```
it follows the same formula of, `<typename> <varname>` however, what is this `[4]`? the square brackets (`[]` if you arent familiar with the namings), signify we are creating a (static, we will explain the difference in [Pointers](<./Pointers.md>) and [Dynamic Memory](<./Dynamic Memory.md)) array of 4 integers 

## How do we use this?
The example array above contains 4 integers, but they don't have names, so how would we access them?

say we wanted to set the *first* element in the array
```c
array[0] = 42; //Notice how i used 0
```

So, lets break this down. Once an array is created we use the square brackets (`[]`) to access the elements inside of it, the number inside the square brackets is called an *Index*, Our array is laid out like this

| 0 | 1 | 2 | 3 |
|---|---|---|---|
| first | second | third | fourth |

notice how the first element is at index 0, most programming languages do it like this so its good to recognize and remember. There are some underlaying reasons as to why, which we will explain in [Pointers](<./Pointers.md>) ()


