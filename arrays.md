# Arrays in rust
    What Is an Array?
    Define an Array
    Access an Element of an Array
    How to Make an Array Mutable?
    Print the Array
    Get the Length of the Array
    Get Slice
        Syntax 
    Quiz 
    
    
    
    
    




# What Is an Array?


an array is a homogenous sequence of elements begin a mopound type it isused when the collection of values of the same type are to e stored ina single variable in rust an array can only be of fixed length like all other languages each element in the array is assigned an index , by default the first element is always at index 0.


# Define an Array
let name: [type;size ] = [value1,value2,value3,....]



# access an element of an array 
any value of the array can be accessed by writing the array name ofollowed by the index number enclosed within square brackets


```rust
fn main() {
   //define an array of size 4
   let arr:[i32;4] = [1, 2, 3, 4]; 
   //print the first element of array
   println!("The first value of array is {}", arr[0]);
   // initialize an array of size 4 with 0
   let arr1 = [0; 4]; 
   //print the first element of array
   println!("The first value of array is {}", arr1[0]);
}
```



# how to get the length of the array

```rust
fn main() {
   //define an array of size 4
   let arr:[i32;4] = [1, 2, 3, 4]; 
   //print the length of array
   println!("The length of array is {}", arr.len());
}
```




# How to Make an Array Mutable?
```rust
fn main() {
   //define an array of size 4
   let mut arr:[i32;4] = [1, 2, 3, 4]; 
   //print the first element of array
   println!("The first value of array is {}", arr[0]);
   //change the first element of array
   arr[0] = 10;
   //print the first element of array
   println!("The first value of array is {}", arr[0]);
}
```


# Print the Array
```rust
fn main() {
   //define an array of size 4
   let arr:[i32;4] = [1, 2, 3, 4]; 
   //print the array
   println!("{:?}", arr);
}
```

# Get Slice
```rust
fn main() {
   //define an array of size 4
   let arr:[i32;4] = [1, 2, 3, 4]; 
   //get the slice of array
   let slice = &arr[1..3];
   //print the slice
   println!("{:?}", slice); // [2, 3]
}
```






