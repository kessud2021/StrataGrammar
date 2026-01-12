# Strata Grammar for GitHub Linguist

A comprehensive grammar definition for the **Strata Programming Language** to enable syntax highlighting and language support on GitHub and other text editors.

## About Strata

Strata is a modern programming language designed to be: 
- **Multi-paradigm**: Supporting both imperative and functional programming
- **Polyglot**:  Compiling to multiple targets (C, JavaScript, WebAssembly)
- **Type-safe**: With optional type annotations
- **Developer-friendly**: Clear syntax inspired by multiple languages

## Strata Language Syntax Overview

### Basic Structure

```str
import io from std::io

func main() => int {
  io.print("Hello, Strata!")
  return 0
}
```

### Imports

Strata supports multiple import forms:

```str
import io from std::io              // Standard library
import math from std::math          // Standard library module
import util from ./util             // Relative path (sibling)
import config from ../config        // Parent directory
import http from myapp::http        // Package import
```

### Variables and Type Annotations

Strata supports explicit type annotations:

```str
let x: int = 42
const name: string = "Strata"
var count: int = 0                  // Mutable variable
let value: float = 3.14
let flag: bool = true
```

### Primitive Types

- **Basic**:  `int`, `float`, `bool`, `char`, `string`, `any`
- **Rust-style signed**:  `i8`, `i16`, `i32`, `i64`
- **Rust-style unsigned**: `u8`, `u16`, `u32`, `u64`
- **Floating point**: `f32`, `f64`
- **Collections**: `array`, `list`, `map`, `dict`, `set`, `tuple`
- **Advanced**: `option`, `result`, `promise`, `void`, `null`, `undefined`
- **Regex**: `regex`, `pattern`
- **Scientific**: `complex`, `matrix`, `dataframe`

### Functions

```str
func add(a: int, b: int) => int {
  return a + b
}

func greet(name: string) => string {
  return "Hello, " + name
}

func processArray(arr: list) => void {
  for (let i:  int = 0; i < arr.length; i++) {
    io.print(arr[i])
  }
}
```

### Control Flow

```str
// If statement
if (x > 10) {
  io.print("x is greater than 10")
}
else if (x == 10) {
  io.print("x is equal to 10")
}
else {
  io.print("x is less than 10")
}

// While loop
while (i < 10) {
  i = i + 1
}

// Break and continue
while (true) {
  if (condition) {
    break
  }
  if (skip) {
    continue
  }
}
```

### Operators

#### Arithmetic
- `+`, `-`, `*`, `/`, `%`

#### Comparison
- `==`, `!=`, `<`, `>`, `<=`, `>=`

#### Logical
- `&&`, `||`, `!`

#### Bitwise
- `&`, `|`, `~`, `^`, `<<`, `>>`

#### Assignment
- `=`, `+=`, `-=`, `*=`, `/=`, `%=`

#### Special
- `=>` (arrow operator for function return types)

### Standard Library Modules

#### std:: io
```str
import io from std::io

io.print("message")      // Print with newline
io.println("message")    // Print with newline
```

#### std::math
```str
import math from std::math

let result: float = math.sqrt(16. 0)
let sine: float = math.sin(3.14159)
let power: float = math.pow(2.0, 3.0)
let absolute: float = math.abs(-5.0)
```

#### std::text
```str
import text from std::text

let upper: string = text.toUpperCase("hello")
let lower: string = text.toLowerCase("WORLD")
let words: list = text.split("hello world", " ")
let joined: string = text.join(["a", "b", "c"], "-")
```

#### std::time
```str
import time from std::time

let now: int = time.now()
let timestamp: int = time.timestamp()
let date: int = time.getDate(now)
```

### Comments

```str
// Single line comment

// Multi-line comments can span
// multiple lines using // on each line
```

## Grammar File Formats

This repository provides grammar definitions in multiple formats:

- **strata.cson** - TextMate grammar format
- **strata.json** - JSON TextMate grammar format

## Installation for GitHub Linguist

To use this grammar with GitHub Linguist, add the grammar files to your repository's `.linguist.yml` or configure via GitHub's built-in language detection. 

## Examples

The `examples/` directory contains sample Strata programs demonstrating: 

- `hello.str` - Basic hello world
- `math_operations.str` - Mathematical functions
- `control_flow.str` - If statements, loops
- `types_and_variables.str` - Type annotations and variables

## Features Supported

✅ Keywords and control structures
✅ Function declarations and calls
✅ Variable declarations (let, const, var)
✅ Type annotations
✅ String literals with escape sequences
✅ Numeric literals (integers and floats)
✅ Comments (single-line)
✅ Import statements
✅ All standard operators
✅ Standard library module highlighting

## Contributing

Contributions are welcome! If you find syntax patterns that aren't properly highlighted, please submit an issue or pull request.

## License

This grammar definition is released under the MIT License. 

## References

- [Strata GitHub Repository](https://github.com/VSS-CO/Strata)
- [GitHub Linguist](https://github.com/github-linguist/linguist)
- [TextMate Grammar Documentation](https://macromates.com/manual/en/language_grammars)

---

**Last Updated**:  2026-01-12
**Strata Version**: Based on latest distribution
