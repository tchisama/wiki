



# indefinite loops - while and loop in rust


## while loop
while loop also iterates until a specific condition is reached , however in the case of a while loop the number of iterations is not known in advance


Syntax:
```rust
while condition {
    // code to be executed
}
```

Example:
```rust
fn main() {
    let mut n = 0;
    while n < 5 {
        println!("n is {}", n);
        n += 1;
    }
}
```

Output:
```
n is 0
n is 1
n is 2
n is 3
n is 4
```

