# Structs
Run of the mill structn should be formatted like this
```rs
struct Foo 
{
    bar : i32
}
```
Structs with lifetimes and generics should be formatted like this
```rs
struct Foo 
<'a, T>
{
    bar : T,
    baz : &'a u8
}
```
Visibility modifiers should be placed on the line before the struct like this
```rs
pub
struct Foo
{
    bar : u8
}
```
Tuple structs should be formatted as like the following
```rs
// No generics/lifetimes
struct Foo (u8, u8)
// With
struct Foo
<'a, T>
(
    &'a T, 
    T
)
```
Visibility modifiers in a strict should look like this
```rs
struct Foo
{
    pub
      bar : u8
}
```

# Functions
Functions with no args should look like this
```rs
fn foo () 
{
    // code here
}
```
Function containing 3 or less args should look like this
```rs
fn foo (bar : i32, baz : i32, fob : i32)
{
    // code here
}
```
3 or more args should be formatted as such
```rs
fn foo (
    bar : i32, baz : i32, fob : i32,
    cob : i32, bob : i32
) 
{
    // code here
}
```
Return types should look like this
```rs
fn foo (bar : i32, baz : i32, fob : i32)
-> i32
{
    // code here
}
```
```rs
fn foo (
    bar : i32, baz : i32, fob : i32,
    cob : i32, bob : i32
) 
-> i32 
{
    // code here
}
```
