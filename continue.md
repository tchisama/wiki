






# what is a continue statement in rust ?

the continue statement , when encountered inside a loop, skips the execution of the rest of the statements in the loop's body for the current iteration and returns the control to the start of the loop,


# example

```rust
fn main() {
    for i in 1..=5 {
        if i == 3 {
            continue;
        }
        println!("i = {}", i);
    }
}

```

# another example 

```rust
 fn main() {
    // define an integer variable
    let mut var = 1; 
    // define a boolean variable
    let mut found = false;
    // define a while loop
    while !found {
      var = var + 1;
      println!("{}", var);
      
      if var == 4 {
          println!("I encoutered a continue statement");
          continue;
        }
        println!("I did not encounter continue statement");
        
        if var == 10{
          found = true;
        }
    }
}
```
