




# Borrowing operator in rust


Borrowing means to reference the original data binding or to share the data .


there is a table showed the difference between borrowing and ownership in rust


| operator                   | operation      | explanation                                  |
| -------------------------  | -------------- | -------------------------------------------- |
| operand 1 = & operand 2    | shared borrow  | operand1 can read data of another operand2   |
| operand 1 = &mut operand 2 | mutable borrow | operand1 can read and write data of operand2 |



example of borrowing in rust 

```rust

fn main() {
    let x = 10;
    let mut y = 13;
    //immutable reference to a variable
    let a = &x;
    println!("Value of a:{}", a); 
    println!("Value of x:{}", x); // x value remains the same since it is immutably borrowed
    //mutable reference to a variable
    let b = &mut y;
    println!("Value of b:{}", b);

    *b = 11; // derefencing 
    println!("Value of b:{}", b); // updated value of b
    println!("Value of y:{}", y); // y value can be changed as it is mutuably borrowed
}


```
