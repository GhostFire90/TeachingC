Strings are essentially an [Array](<./Arrays.md>) of characters with the last element being a NUL terminator which is essentially just the hex value 0x00. The reason it is done this way is most of c's standard functions (printf, strlen, strcmp, etc.) need a way to know when the string ENDS without knowing how long it is.

```c
const char* message
```