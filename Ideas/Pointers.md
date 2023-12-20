Pointers in all technicality are their own type. Think of them like your home address sort of thing, to tell someone where you live, you give them the address to your house.

All a pointer is, is an address to where some chunk of data lives, it is declared like so

```c
<typename>* varname;
```
the star is important, that is how you know its a pointer.
```c
int* i;
```
that basically means "i is an address that *points* to where an integer lives"