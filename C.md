# Lemon's C Style Guide

## Naming
All non macro identifiers should be in snake case; Except enum fields should be screaming snake case.

## Functions

### No args
```c
int
foo ()
{
    // code here
}
```
### 3 or less args*
```c
int
foo (int bar, int baz)
{
    // code here
}
```
### 3 or more args*
```c
int
foo 
(
    int bar, int baz, int fob,
    int cob
)
{
    // code here
}
```
*\*Note that if your function takes exactly three arguments, you may do whichever of the above you prefer.*
### Function Calls
```c
int
foo ()
{
    // code here
}

foo();
```

## Casts, Pointers and Const

### Pointers
Should **always** be left aligned.
```c
char* foo = "bar";
char const* bar = "foo";
```
### Casts
```c
void* foo = (void*) "Hello";
char const* bar = (void const*) "Bye";
```
## Goto labels
```c
int
main ()
{
TRY_AGAIN;
    if (1) 
    {
        goto RETURN;
    } 
    else 
    {
        goto TRY_AGAIN;
    }
RETURN:
    return 0;
}
```
## Branching
### If
```c
if (1)
{
    // code here
}
```
### If Else
```c
if (1)
{
    // code here
}
else
{
    // code here
}
```
### Switch Case
```c
switch (1)
{
case 1:
    // code here
default:
    // code here
}
```
### While
```c
while (1)
{
    // code here
}
```
### Do While
```c
do 
{
    // code here
}
while (1);
```
