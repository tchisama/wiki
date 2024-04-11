





# returning multiple values from a function in rust


in system `programming` languages like c++ and c , it is only possible to return a sigle value or a pointer to an array from a function. However, Rust allows you to return multiple values using a tuple.

```rust
fn get_two_values() -> (i32, i32) {
    (10, 20)
}
fn main () {
    let (a, b) = get_two_values();
    println!("a = {}, b = {}", a, b);
}
```
