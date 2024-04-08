




# Bitwise operators in rust


## what are bitwise operators ?

bitwise operators deal with the binary representation of the operands.

example:

```rust
let a = 5; // 101
let b = 3; // 011

let c = a & b; // 001
let d = a | b; // 111
let e = a ^ b; // 110
let f = !a;    // 11111111111111111111111111111010
```




example unix file permissions:

```

7 => 111 => rwx => read, write, execute
6 => 110 => rw- => read, write
5 => 101 => r-x => read, execute
4 => 100 => r-- => read
3 => 011 => -wx => write, execute
2 => 010 => -w- => write
1 => 001 => --x => execute
0 => 000 => --- => none

```


# &

** 7 & 6 **

| 7 | 6 | & |
|---|---|---|
| 1 | 1 | 1 |
| 1 | 1 | 1 |
| 1 | 0 | 0 |
|---|---|---|

you can use it to check if the user have permissions

```rust
let user = 7;
let read = 4;
let write = 2;
let execute = 1;

let user_permissions = 6;

if user_permissions & read == read {
    println!("user can read");
}else{
    println!("user can't read");
}
```

# |

** 5 | 6 **

| 5 | 6 | \| |
|---|---|----|
| 1 | 1 | 1  |
| 0 | 1 | 1  |
| 1 | 0 | 1  |
|---|---|----|

you can use it to add permissions

```rust
let user = 5;
let read = 4;
let write = 2;
let execute = 1;

let mut user_permissions = 0;

user_permissions = user_permissions | read; // add read permission
user_permissions = user_permissions | write; // add write permission
user_permissions = user_permissions | execute; // add execute permission

println!("user permissions: {}", user_permissions);
```








