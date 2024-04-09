




#what is a for loop ?
a for loop is a definite loop meaning the number of iterations is defined before the loop begins.

syntax:

```rust
for variable in range {
    // code to be executed
}
```
example:
```rust
fn main() {
    for _i in 0..5 {
        println!("Hello, world!");
    }
}]]
```

another example:
```rust
fn main(){
    for (count, variable) in (7..10).enumerate(){
        println!("count = {},variable = {}",count,variable);
    }
}
```
