
## Topics Used
- [Arrays](<./../Ideas/Arrays.md>)
- [Loops](<./../Ideas/Loops.md)
- [Functions](<./../Ideas/Functions.md>)
- [Pointers](<./../Ideas/Pointers.md>)
## Assignment 

Write a function that sums 2 arrays
```c
int array_sum(const int* a1, const int* a2, int length);
```

Compile with
```bash
clang <filename> -Wall -Wextra -o lab1.out
```

### Ex:
```
array_sum({1, 2, 3}, {4, 5, 6}, 3) = 21
```

### Considerations
- What if one array is smaller than the other?
- What if either of the arrays are [`NULL`](<./../Ideas/Pointers.md#NULL>)  
- What if length is negative? how should we go about fixing this?
### Assumptions
- Assume the length is as long as the shortest array, dont worry about it being longer

