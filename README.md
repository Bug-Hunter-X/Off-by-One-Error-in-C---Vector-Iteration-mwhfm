# Off-by-One Error in C++ Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating through a `std::vector`. The error occurs when the loop condition `i <= vec.size()` is used, which attempts to access an element beyond the valid range of indices.

## Bug Description
The `bug.cpp` file contains a `for` loop that iterates through a `std::vector` of integers.  The loop condition is `i <= vec.size()`, which is incorrect.  Vector indices are zero-based, so the last valid index is `vec.size() - 1`.  Accessing `vec[vec.size()]` leads to undefined behavior, potentially causing a crash or unexpected results.

## Bug Solution
The `bugSolution.cpp` file corrects the loop condition to `i < vec.size()`, ensuring that the loop only iterates through valid indices.  This simple change prevents the off-by-one error.