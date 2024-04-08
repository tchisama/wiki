    What Are Constant Variables?
    Syntax
    Example
    Difference Between const and let Variables
            Declaration
            Scope
            Mutability
            Data Type
            Set Value at Run-time
            Shadowing
            
            
            
            
            
            
            
# What Are Constant Variables?



constant variables are ones that are declared constant throughtout the program scope , meaning their value cannot be modified , they can be definded in global and local scope.



# Syntax

```rust
const NAME: i32 = 002;
```

naming convention : by convention you write a constant variable name in screaming_snake_case.

    . all letters should be upper case.
    . all words should be separate using an underscore (_)
  
  
  
# Example 

the following expample deines two const variables:
golbal and local

```rust
const ID_1: i32 = 4; // define a global constant variable
fn main() {
    const ID_2: u32 = 3; // define a local constant variable
    println!("ID:{}", ID_1); // print the global constant variable
    println!("ID:{}", ID_2); // print the local constant variable
}
```















