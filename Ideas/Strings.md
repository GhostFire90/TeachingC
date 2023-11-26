Strings are essentially an [Array](<./Arrays.md>) of characters with the last element being a NUL terminator which is essentially just the hex value 0x00. The reason it is done this way is most of c's standard functions (printf, strlen, strcmp, etc.) need a way to know when the string ENDS without knowing how long it is.

```c
const char* message = "hello";
```

this is laid out in array format like 

| 0 | 1 | 2 | 3 | 4 | 5 |
| :---: | :---: | :---: | :---: | :---: | :---: |
|'h'|'e'|'l'|'l'|'0'|'\\0'|
where the [Escape Sequence](<./../Explanations/Escape Sequences.md>) '\\0' represents the nul terminator, aka 0 
