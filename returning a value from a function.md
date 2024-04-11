




# returning a value from a function in rust

```rust
fn main() {
    let x = five();
    println!("The value of x is: {}", x);
}

fn five() -> i32 {
    5
}
```
Example:

```rust
fn square(n:i32)->i32{
  println!("The value of n inside function : {}", n);
  let m = n * n;
  m // return the square of the number n
}  
fn main() {
  let  n = 4;
  println!("The value of n before function call : {}", n);
  println!("Invoke Function");
  println!("\nOutput : {}",square(n));
}
```
