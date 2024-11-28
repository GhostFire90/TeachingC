When working with C you tend to work with a lot of functions you dont write (such as [printf](<./../Explanations/Basic Printf.md)), however the compiler still needs to know its [prototype](<./Functions.md#Function Prototypes>), though copying the prototype to the top of every file you work on gets very annoying very fast. This is what Includes are for

## Syntax
there are two forms of include, local and include-path, we will cover the latter first
```c
#include <stdio.h>
```
include-path includes use triangle brackets (`<>`) and only look in the given include path. The compiler usually sets this up to some directory on your system where things are installed. However you can add to this path with the `-I` flag on your compiler instructions
```c
#include "foo.h"
```
local is a bit more complex, it first checks the path relative to current file, in this case, look for `foo.h` in the current folder, then it checks the paths as specified above. however it is best practice to only use it for relative paths for clarity.

## What does it do?
this is called a preprocessor a directive which we will cover when we talk about compilers. Basically what it does is it replaces include line with the contents of the  `.h` file before compiling so *everything* you put in there will be copy pasted. For basic uses you should ***only*** place function prototypes in header files (`.h`) 
