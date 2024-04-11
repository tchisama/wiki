






# what is arguments pass by refernce 
when we want to called function to make changes to the parametrs such that the chabges are seen by the calling function when the call returns.


! important , its effecting the varibales it self when u use this mithod

Example:

```rust 
fn square(n:&mut i32){
  *n = *n * *n;
  println!("The value of n inside function : {}", n);
}  
fn main() {
  let  mut n = 4;
  println!("The value of n before function call : {}", n);
  println!("Invoke Function");
  square(&mut n);
  println!("The value of n after function call : {}", n);
}
```

# output

```rust
The value of n before function call : 4
Invoke Function
The value of n inside function : 16
The value of n after function call : 16
```



