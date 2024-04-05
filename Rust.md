
### Rust Cheat Sheet

#### 1. Basic Syntax

```rust
// Variables
let x: i32 = 5;
let mut y = 10; // Mutable variable

// Constants
const PI: f64 = 3.14159;

// Functions
fn add(a: i32, b: i32) -> i32 {
    a + b
}

// Control Flow
if condition {
    // code
} else if another_condition {
    // code
} else {
    // code
}

// Loops
while condition {
    // code
}

for item in iterable {
    // code
}

// Data types
let boolean: bool = true;
let integer: i32 = 42;
let float: f64 = 3.14;
let character: char = 'a';
let string: &str = "Hello, Rust!";

// Tuples
let tuple: (i32, f64, &str) = (42, 3.14, "Hello");

// Arrays
let array: [i32; 5] = [1, 2, 3, 4, 5];

// Slices
let slice: &[i32] = &array[1..3];

// Vectors
let mut vector: Vec<i32> = Vec::new();
vector.push(1);
vector.push(2);

// Structs
struct Point {
    x: i32,
    y: i32,
}
let point = Point { x: 0, y: 0 };

// Enums
enum Direction {
    Up,
    Down,
    Left,
    Right,
}
let direction = Direction::Up;

// Traits
trait Drawable {
    fn draw(&self);
}

// Implementing Traits
impl Drawable for Point {
    fn draw(&self) {
        println!("Drawing point at ({}, {})", self.x, self.y);
    }
}
```

#### 2. Ownership, Borrowing, and Lifetimes

```rust
// Ownership
let s = String::from("hello"); // s is the owner of the String
let s2 = s.clone(); // deep copy of s, now s2 is owner

// Borrowing
fn calculate_length(s: &String) -> usize { // s is a reference to a String
    s.len()
} // s goes out of scope but nothing happens to the actual String

// Mutable Borrowing
fn add_one(x: &mut i32) {
    *x += 1; // * dereferences the pointer
}

// Lifetimes
fn longest<'a>(x: &'a str, y: &'a str) -> &'a str { // 'a denotes lifetime
    if x.len() > y.len() {
        x
    } else {
        y
    }
}
```

#### 3. Error Handling

```rust
// Result
fn parse_int(s: &str) -> Result<i32, ParseIntError> {
    s.parse::<i32>()
}

// Option
fn divide(a: f64, b: f64) -> Option<f64> {
    if b == 0.0 {
        None
    } else {
        Some(a / b)
    }
}

// Pattern Matching
match result {
    Ok(value) => println!("Parsed value: {}", value),
    Err(error) => println!("Error: {}", error),
}
```

#### 4. Concurrency

```rust
use std::thread;
use std::time::Duration;

fn main() {
    let handle = thread::spawn(|| {
        for i in 1..=5 {
            println!("spawned thread: {}", i);
            thread::sleep(Duration::from_millis(1000));
        }
    });

    for i in 1..=3 {
        println!("main thread: {}", i);
        thread::sleep(Duration::from_millis(500));
    }

    handle.join().unwrap();
}
```

#### 5. Macros

```rust
macro_rules! greet {
    () => {
        println!("Hello, Rust!");
    };
}

fn main() {
    greet!(); // Prints "Hello, Rust!"
}
```

