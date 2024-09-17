# School 21. Matrix+

Implementation of the `s21_matrix_oop.h` library for matrix operations using Object-Oriented Programming (OOP) principles in C++.

## Features Overview

| Operation                   | Description                                        | Exceptional Situations                               | Status |
| --------------------------- | -------------------------------------------------- | --------------------------------------------------- |--------|
| `bool EqMatrix`             | Checks matrices for equality.                      | -                                                   |   ☑️   |
| `void SumMatrix`            | Adds another matrix to the current one.            | Different matrix dimensions.                        |   ☑️   |
| `void SubMatrix`            | Subtracts another matrix from the current one.     | Different matrix dimensions.                        |   ☑️   |
| `void MulNumber`            | Multiplies the current matrix by a number.         | -                                                   |   ☑️   |
| `void MulMatrix`            | Multiplies the current matrix by another matrix.   | The number of columns in the first matrix is not equal to the number of rows in the second matrix. |   ☑️   |
| `S21Matrix Transpose`       | Returns a transposed version of the matrix.        | -                                                   |   ☑️   |
| `S21Matrix CalcComplements` | Calculates the algebraic complement of the matrix. | The matrix is not square.                           |   ☑️   |
| `double Determinant`        | Calculates the matrix's determinant.               | The matrix is not square.                           |   ☑️   |
| `S21Matrix InverseMatrix`   | Returns the inverse of the matrix.                 | Matrix determinant is 0.                            |   ☑️   |

## Constructors and Destructors

| Method                         | Description                                        | Status |
| ------------------------------ | -------------------------------------------------- |--------|
| `S21Matrix()`                  | Basic constructor initializing a default matrix.   |   ☑️   |
| `S21Matrix(int rows, int cols)`| Constructor with specified rows and columns.       |   ☑️   |
| `S21Matrix(const S21Matrix& other)` | Copy constructor.                        |   ☑️   |
| `S21Matrix(S21Matrix&& other)` | Move constructor.                                 |   ☑️   |
| `~S21Matrix()`                 | Destructor.                                        |   ☑️   |

## Operator Overloading

| Operator                      | Description                                        | Exceptional Situations                               | Status |
| ----------------------------- | -------------------------------------------------- | --------------------------------------------------- |--------|
| `+`                           | Addition of two matrices.                          | Different matrix dimensions.                        |   ☑️   |
| `-`                           | Subtraction of one matrix from another.            | Different matrix dimensions.                        |   ☑️   |
| `*`                           | Multiplication of matrices or by a number.         | Number of columns in the first matrix does not equal the number of rows in the second matrix. |   ☑️   |
| `==`                          | Checks for matrix equality (`EqMatrix`).           | -                                                   |   ☑️   |
| `=`                           | Assignment of one matrix to another.               | -                                                   |   ☑️   |
| `+=`                          | Addition assignment (`SumMatrix`).                 | Different matrix dimensions.                        |   ☑️   |
| `-=`                          | Subtraction assignment (`SubMatrix`).              | Different matrix dimensions.                        |   ☑️   |
| `*=`                          | Multiplication assignment (`MulMatrix`/`MulNumber`).| Number of columns in the first matrix does not equal the number of rows in the second matrix. |   ☑️   |
| `(int i, int j)`              | Indexing matrix elements (row, column).            | Index is outside the matrix.                        |   ☑️   |

## Run Locally

### Prerequisites

- A C++ compiler (`gcc` recommended).
- The `GTest` library for unit testing.

### Steps

1. **Clone the repository**

    ```bash
    git clone git@github.com:kmiakaeva/S21-matrix-cpp.git
    ```

2. **Navigate to the project directory**

    ```bash
    cd S21-matrix-cpp/src
    ```

3. **Build the library**

    ```bash
    make
    ```

4. **Run tests**

    ```bash
    make test
    ```

5. **Clean build files**

    ```bash
    make clean
    ```
