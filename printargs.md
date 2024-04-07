



you can print line in rust with println! macro

```rust
fn main() {
    println!("Hello, world!");
}
```


rust only print string if you want to print variables or numbers you need to use {} in the string and pass the variable as argument to the println! macro

```rust
fn main() {
    let x = 5;
    println!("The value of x is: {}", x);
}
```

and if you want to print multiple variables you can pass them as arguments to the println! macro

```rust
fn main() {
    let x = 5;
    let y = 10;
    println!("The value of x is: {} and y is: {}", x, y);
}
```
you can named the variables in the println! macro 
like that 

```rust
fn main() {
    println!("The value of x is: {x} and y is: {y}", x=10, y=32);
}
```


ok now what if you want to convert the value to binary hexedicimal or octal you can do that by using :b for binary ...


```rust
fn main() {
    let x = 10;
    println!("The value of x is: {x} in binary is: {x:b}", x=x);
}
```

you can use debug trait and write as many valuese as desired within the parenthese


```rust
fn main() {
    let x = 10;
    let y = 20;
    println!("{:?}", (10,"hello world"));
}
```
