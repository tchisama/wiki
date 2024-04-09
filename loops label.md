







# what is a loop label in rust ?

a loop label assigns an identifier to a loop .



syntax : 

```rust
fn main() {
 'outer:for i in 1..5 { //outer loop
    println!("Muliplication Table : {}", i);
   'inner:for j in 1..5 { // inner loop
        if i == 3 { continue 'outer; } // Continues the loop over `i`.
        if j == 2 { continue 'inner; } // Continues the loop over `j`.
        println!("{} * {} = {}", i, j, i * j);
   }
 }
}
``` 







```rust
fn main (){
   let mut i = 
}


fn factorial(n) -> i32 {
  let mut result = 1;
  for i in 1..=n {
    result *= i;
  }
  result
}
```








