




# Rust variables




```
let language;
```



#what is binding ? 

Rust refers to declarations as bindings as they bind a nameat the time of creation . let is a kind of decalaration statement



# Naming conventions



by convention you would write a variable name in a snake_case i.e

all letters should be lower case 
all words should be separated using an underscore



# What if you want to make variable mutable ?

```
let mut language = "Rust";
```
so now you can stuff like this 

fn main() {
    let mut language = "Rust"; // define a mutable variable
    println!("Language: {}", language); // print the variable
    language = "Java"; // update the variable
    println!("Language: {}", language); // print the updated value of variable
}




# now lets assign multiple variables 
its is possible ito assign multiple variables in one statement

```
let (a, b) = (1, 2);
```




## note : if a variable is kept un-assigned or unused , you'll get a warning ,

to remove such a warning write the expression 

```
#[allow(unused_variables,unused_mut)]
```
that way you will get off the warning.





# Rust Scope and shadowing


## scope of variable 
there are two types of variables in rust 
1. global variable
2. local variable


## global variable
global variable are declared outside the main function and are accessible throughout the program

```
let global
```

## local variable
local variable are declared inside the main function and are accessible only within the main function

```
fn main() {
    let local = "local variable";
    println!("{}", local);
}
```











