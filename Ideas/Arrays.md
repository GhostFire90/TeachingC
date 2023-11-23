Arrays in C have some funky ties to [Pointers](/Ideas/Pointers.md) so this will be more of a general overview of arrays.


## What are they
Arrays are most commonly, a collection of [variables](/Ideas/Variables.md) of the same type. so instead of having

```c
int a;
int b;
int c;
int d;
```

we could have an array of integers that is 4 big
```c
int abcd[4];
```


## How do we use this?
Arrays you cant reference exactly like variables, they are laid out sorta like this

| 0 | 1 | 2 | 3 |
|---|---|---|---|
| ... | ... | ... | ... |


