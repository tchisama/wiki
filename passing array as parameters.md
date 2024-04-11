





# functioons with arrays as arguments in rust ?




example:

```rust
fn main() {
    let arr = [1, 2, 3, 4, 5];
    let result = sum(&arr);
    println!("Sum of array is {}", result);
}

fn sum(arr: &[i32]) -> i32 {
    let mut sum = 0;
    for i in arr.iter() {
        sum += i;
    }
    sum
}
```


# pass by reference 

```rust
fn main() {
    let arr = [1, 2, 3, 4, 5];
    let result = sum(&arr);
    println!("Sum of array is {}", result);
}

fn sum(arr: &[i32]) -> i32 {
    let mut sum = 0;
    for i in arr.iter() {
        sum += i;
    }
    sum
}
```







