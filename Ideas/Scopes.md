
Common phases that will be used in this "course" reference scope, such as
1. In scope
2. Out of scope
3. going out of scope
So what is a scope?

## What is it
Think of a scope as a little box that you open, put things in and close.
Every scope has:
1. A beginning (Opening the box)
2. A body (putting things in and doing things with the things inside the box)
3. An end (closing the box)

Some example in code
```c
{ // OPEN DA BOX
	int x = 1;
	x = x * 2;
} // CLOSE DA BOX
```

### Why are they important
Variables are only accessible in their current scope, so in the above example and following the metaphor, once you close the box, its contents are no longer accessible

## Nested scopes
```c
{
	//b and c arent accessible
	int a;
	{
		// a and b are accessible
		int b;
	}
	{
		// a and c are accessible
		int c;
		{
			// a, c, and d are accessible
			int d;
		}
	}
}
```

While in the above examples I'm only doing free-standing scopes, every time you see curly braces (`{}`) that is a scope, whether it is a conditional, function, or loop, that is a scope

### Phrases
So back to the phrases mentioned in the beginning