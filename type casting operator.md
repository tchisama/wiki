







# type casting operator in rust 

What is type casting operator ?


Type casting operator is when you convert the data type of the variable to some other data type.

type casting in rust 



in rust typecastin g is done using the ** as ** keyword followed by the desired data type of the variable or value

```rust
fn main() {
    let a = 15;
    let b = (a as f64) / 2.0; 
    println!("a: {}", a);
    println!("b: {}", b);
}
```

# what data types cannot be type casted ?

strings &str or character cannot be type casted to the data type of type integer or float
```rust
fn main() {
    let a: char = 'r' ; // cannot be type casted
    let b = a as &str ; 
    println!("a: {}", a);
    println!("b: {}", b);
}
```

