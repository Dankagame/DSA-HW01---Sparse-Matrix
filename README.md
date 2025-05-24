DSA-HW01 - Sparse Matrix Implementation
Overview
This project implements a SparseMatrix class in Python for efficient storage and manipulation of sparse matrices. It supports reading matrices from files, performing operations (addition, subtraction, multiplication), and saving results. The implementation uses a dictionary to store only non-zero elements, optimizing memory usage for large, sparse matrices.
Features

Matrix Initialization: Create a sparse matrix with specified dimensions.
File Input: Read sparse matrices from a text file in a specific format.
Element Access/Modification: Get or set elements at specific (row, col) indices.
Matrix Operations:
Addition of two sparse matrices.
Subtraction of two sparse matrices.
Multiplication of two sparse matrices.


Error Handling: Validates input file formats and matrix dimensions, raising ValueError or IndexError for invalid inputs.
Interactive CLI: Allows users to select matrix files, choose operations, and save results.

Requirements

Python 3.x
No external libraries required

File Structure

main.py: Core implementation of the SparseMatrix class and CLI interface.
file1.text, file2.text: Example input files containing sparse matrix data (not included by default; create as needed).
README.md: This documentation file.

Input File Format
The input files (e.g., file1.text, file2.text) must follow this format:
rows=<number_of_rows>
cols=<number_of_columns>
(row, col, value)
(row, col, value)
...

Example:
rows=3
cols=4
(0, 1, -694)
(1, 2, 857)
(2, 0, 123)


First line: rows=<integer> (number of rows).
Second line: cols=<integer> (number of columns).
Subsequent lines: Tuples (row, col, value) for non-zero elements.
Invalid formats (e.g., extra whitespace, missing parentheses, non-integer values) raise a ValueError: Invalid file format.

Usage

Run the Program:
python3 main.py


Follow the CLI Prompts:

Choose an operation: 1 (add), 2 (subtract), or 3 (multiply).
Enter 1 to specify the first matrix file path, then provide the path (e.g., file1.text).
Enter 2 to specify the second matrix file path, then provide the path (e.g., file2.text).
View the result printed in the console.
Optionally save the result to a file by entering y and providing an output file path.


Example Interaction:
Sparse Matrix Calculator
-----------------------
Available Operations:
1. Add two matrices
2. Subtract two matrices
3. Multiply two matrices
Choose an operation (1, 2, or 3): 1
Select matrix files:
Enter 1 to specify the first matrix file path: 1
Enter the path for the first matrix file: file1.text
Enter 2 to specify the second matrix file path: 2
Enter the path for the second matrix file: file2.text
Addition completed successfully.
Result:
rows=3
cols=4
(0, 1, -694)
(1, 2, 857)
Would you like to save the result to a file? (y/n): y
Enter the output file path: result.txt
Result saved to result.txt



Creating Input Files
To test the program, create text files (e.g., file1.text, file2.text) with the correct format. Example:
echo -e "rows=3\ncols=4\n(0, 1, -694)\n(1, 2, 857)" > file1.text
echo -e "rows=3\ncols=4\n(1, 2, 123)\n(2, 0, 456)" > file2.text

Git Setup
To version control this project, initialize a Git repository and push to GitHub:
git init
echo "# DSA-HW01 - Sparse Matrix" > README.md
git add README.md main.py file1.text file2.text
git commit -m "Initial commit with SparseMatrix implementation"
git branch -M main
git remote add origin https://github.com/Dankagame/DSA-HW01---Sparse-Matrix.git
git push -u origin main

Notes

Ensure matrix dimensions are compatible for operations:
Addition/Subtraction: Matrices must have the same dimensions.
Multiplication: The number of columns in the first matrix must equal the number of rows in the second.


The output file format matches the input format, with elements sorted by column index, then row index.
Error messages are descriptive (e.g., "Invalid file format", "Index out of bounds") to aid debugging.

Contributing
Feel free to fork this repository, make improvements, and submit pull requests. Issues or suggestions can be reported on the GitHub repository.
License
This project is licensed under the MIT License.
