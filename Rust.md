# Lemon's Rust Style Guide

## Structs

### Structs Without Generics Or Lifetimes

```rs
struct Foo
{
    bar : i32
}
```

### Structs With Lifetimes And Generics

```rs
struct Foo
<'a, T>
{
    bar : T,
    baz : &'a u8
}
```

### Struct Visibility Modifiers

```rs
pub
struct Foo
{
    bar : u8
}
```

### Tuple Structs

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

### Member Visibility Modifiers

```rs
struct Foo
{
    pub
      bar : u8
}
```

## Functions

### Functions With No Arguments
```rs
fn foo ()
{
    // code here
}
```

### Functions With Three\* Or Fewer Arguments

```rs
fn foo (bar : i32, baz : i32, fob : i32)
{
    // code here
}
```

### Functions With Three\* Or More Arguments

```rs
fn foo
(
    bar : i32, baz : i32, fob : i32,
    cob : i32, bob : i32
)
{
    // code here
}
```

\**Note that if your function takes exactly three arguments, you may do whichever
of the above you prefer.*

### Return Types

```rs
fn foo (bar : i32, baz : i32, fob : i32)
-> i32
{
    // code here
}
```

```rs
fn foo
(
    bar : i32, baz : i32, fob : i32,
    cob : i32, bob : i32
)
-> i32
{
    // code here
}
```
