    What are Tuples?
    Define a Tuple
        Syntax 1
        Syntax 2
    Example
    Access the Value of the Tuple
    How to Make a Tuple Mutable?
    Print the Tuple
    Quiz
    
    
    
    



# Whhat are tuples?


tuples are heterogeneous sequence of elements meaning each elelment in a tuple can have different data type , Just like arrays , tuples are of a fixed length,


# Define a Tuple

```rust
let tuple_name = (500 ,"hello world", 6.4, 1);
```
```rust
let tuple_name :(i32, &str, f64, i32) = (500 ,"hello world", 6.4, 1);
```



# Access the value of the tuple



tuplename.indexvalue


so for Example

```rust
let tuple_name = (500 ,"hello world", 6.4, 1);
println!("The value at index 0 is : {}", tuple_name.0);
println!("The value at index 1 is : {}", tuple_name.1);
println!("The value at index 2 is : {}", tuple_name.2);

```


# how to make a tuple mutable?

just like a variable becomes mutable by adding the mut keyword after let the same goes for a tuple,

```rust
let mut tuple_name = (500 ,"hello world", 6.4, 1);
tuple_name.0 = 600;
println!("The value at index 0 is : {}", tuple_name.0);
```

















