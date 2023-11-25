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

Arrays are 

| 0 | 1 | 2 | 3 |
|---|---|---|---|
| ... | ... | ... | ... |


