



# if expression 



if expression takes a condition if the condition within the if expression evaluates to be true then the block of code is executed.

code : ➡️

```rust
fn main() {
    let x = 5;
    if x == 5 {
        println!("x is five!");
    }
}
```



if else expression 

in an if else condstruct , if the condition within the if expression evaluates to be false , then the statement within the else block is executed.

code : ➡️

```rust
fn main() {
    let x = 5;
    if x == 5 {
        println!("x is five!");
    } else {
        println!("x is not five :(");
    }
}
```



if else if expression 

if there are mulitple conditions to be checked , then if .. eslse if .. else construct is used.

code : ➡️

```rust
fn main() {
    let x = 5;
    if x == 5 {
        println!("x is five!");
    } else if x == 6 {
        println!("x is six!");
    } else {
        println!("x is not five or six :(");
    }
}
```






# nested if expression 
an  if expression inside the body of another if construct , the general syntax is : 


# short hand if expression

instead o writing a lengthy if-esle construct , we can use a shorthand if .


syntax ➡️

```rust
let result = if condition { value } else { value };
```
another example ➡️

```rust
fn main() {
    let x = "Rust";

    let y: bool = if x == "Rust" { true } else { false };

    // let z: bool = if x == "Rust" { true; } else { false; };

    println!("x:{}", x);
    println!("y:{}", y);

}
```






