





# what is match expression in rust

Match expression checks if the current value corresponds to any vallue within he list of values .
match expression are silmilar to switch statement in other programing languages . like js

```rust
fn main() {
    let number = 13;
    match number {
        1 => println!("It is one"),
        2 => println!("It is two"),
        3 => println!("It is three"),
        4 => println!("It is four"),
        5 => println!("It is five"),
        6 => println!("It is six"),
        7 => println!("It is seven"),
        8 => println!("It is eight"),
        9 => println!("It is nine"),
        10 => println!("It is ten"),
        _ => println!("It is something else"),
    }
}
```
