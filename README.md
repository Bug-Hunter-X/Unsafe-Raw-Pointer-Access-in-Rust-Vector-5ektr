# Unsafe Raw Pointer Access in Rust Vector

This repository demonstrates a potential bug involving unsafe raw pointer access in Rust when working with vectors. Modifying a vector through a raw pointer without proper synchronization or memory management can lead to undefined behavior.

## Bug Description
The `bug.rs` file contains code that directly manipulates a vector using a raw pointer obtained via `as_mut_ptr()`. This approach bypasses Rust's memory safety guarantees, potentially causing data races, memory corruption, or other unpredictable issues.

## Solution
The `bugSolution.rs` file shows a safer way to modify the vector, avoiding unsafe operations.  This example uses standard vector methods to achieve the desired modification, preserving Rust's safety guarantees.