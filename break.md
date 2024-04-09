




# what is a break statement in rust?

The break statement terminates the loop . it is generally placed inside a conditional statement so that the lop terminates if the associated condition is true

Example:

```rust
fn main() {
    let mut counter = 0;

    let result = loop {
        counter += 1;

        if counter == 10 {
             break counter * 2;
        }
    };

    assert_eq!(result, 20);
}
```

