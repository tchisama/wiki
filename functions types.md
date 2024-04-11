


1. main function
2. user defined function



examples:

```rust
fn main(){
    println!("hello world");
}
```

```rust
fn add(a:i32,b:i32)->i32{ // function defined 
    return a+b;
}
fn main(){ // main function
    let a = 10;
    let b = 20;
    let c = add(a,b);
    println!("sum is {}",c);
}
```








