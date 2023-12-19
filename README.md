# MiniGrep

MiniGrep is a simple, command-line application built in Rust, inspired by the functionality of the classic Unix `grep` command. It allows searching for a string within a file, optionally ignoring case. Designed to demonstrate basic Rust concepts, error handling, and environment interaction, it's a perfect learning tool for those new to the language.

## Features

- Search for a string within a file.
- Case-sensitive and case-insensitive search modes.
- Reads environment variable to determine case sensitivity.

## Requirements

- [Rust](https://www.rust-lang.org/tools/install)

## Installation

This application is written in Rust, so you'll need Rust installed on your computer to build it. If you don't have Rust installed, you can download it from [rust-lang.org](https://www.rust-lang.org/tools/install).

To install this project, follow these steps:

1. Clone the repository to your local machine:
   
   ```
   git clone https://github.com/SonikSeven/minigrep.git
   ```
   
2. Navigate to the cloned repository:
   
   ```
   cd minigrep
   ```

3. Build the project with Cargo:
   
   ```
   cargo build --release
   ```

## How to Run

Run the executable in `./target/release/`.

## Usage

Functional usage of MiniGrep requires specifying the query string and the file path as command-line arguments. Case sensitivity is controlled by an environment variable.

- **Basic Command**:
  
   ```
   ./minigrep query_string file_path
   ```

- **Case Insensitive Search**:
  
  Set the `IGNORE_CASE` environment variable before running MiniGrep.
   
   **Linux/Mac**:
   
   ```
   IGNORE_CASE=1 ./minigrep query_string file_path
   ```
   
   **Windows Command Line**:
   
   ```
   set IGNORE_CASE=1
   ./minigrep query file_path
   ```

### Examples

- To search for "rust" in "file.txt":
  
  ```
  ./minigrep rust file.txt
  ```

- To perform a case-insensitive search for "rust" in "file.txt":
  
   **Linux/Mac**:
   
   ```
   IGNORE_CASE=1 ./minigrep rust file.txt
   ```

   **Windows Command Line**:
   
   ```
   set IGNORE_CASE=1
   ./minigrep rust file.txt
   ```

## Testing

MiniGrep comes with unit tests for its search functionalities. Run the tests with Cargo:

```
cargo test
```

This will execute both case-sensitive and case-insensitive search tests.

## About

This project is based on content from "The Rust Programming Language" book by Steve Klabnik and Carol Nichols. The book is an excellent resource for learning Rust, and this project aims to implement some of the concepts and examples presented in the book.

## Attribution

- **Book Title**: The Rust Programming Language
- **Authors**: Steve Klabnik and Carol Nichols
- **Publisher**: No Starch Press
- **Website**: [The Rust Programming Language](https://doc.rust-lang.org/book/)

## License

This project is licensed under the [CC-BY 4.0 License](LICENSE.txt).
