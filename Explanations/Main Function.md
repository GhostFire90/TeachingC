Every C program needs a *main* function. We wont cover exactly what a function is in this page but we will in [Functions](<./../Ideas/Functions.md>)

# What is it

```c
int main(void){
	return 0;
}
```

this program by itself does nothing but it is the simplest c program you can write.

The main function has one purpose: Serve as the start of the program. Everything that is within the curly-braces (`{}` if you don't know the namings) gets run when the program starts, without it the program **will not compile**

# Extras

There are actually 2 variations of the main function, 
```c
int main(void){
	return 0;
}
```
as we mentioned previously as well as
```c
int main(int argc, const char** argv){
	return 0;
}
```