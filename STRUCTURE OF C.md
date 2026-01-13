The structure of a C program is ==divided into several logical sections==, which helps in organizing code, enhancing readability, and promoting modularity. The only mandatory section in every C program is the `main()` function. 

The typical sections of a C program, in order of appearance, are: 

1. **Documentation Section** This optional section includes comments (`//` for single-line or `/* ... */` for multi-line) to provide an overview of the program, such as its purpose, author, and creation date. The compiler ignores these comments.
    - _Example:_ `/* Program to add two numbers */`
2. **Preprocessor Directives (Link Section)** This section contains instructions for the C preprocessor, which processes the source code before the actual compilation.
    - `#include` is used to link necessary header files (e.g., `<stdio.h>` for standard input/output functions like `printf()` and `scanf()`).
    - `#define` is used to define symbolic constants or macros (e.g., `#define PI 3.14159`).
3. **Global Declaration Section** This optional section declares variables, functions, and data types (like structures) that are accessible to all functions within the program. Global variables should be used cautiously.
4. **`main()` Function Section** This is the **mandatory** part of every C program, and program execution begins here. It typically has a declaration part (local variables) and an executable part (the core logic and function calls) enclosed within curly braces `{}`.
    - _Example:_ `int main() { ... return 0; }`
5. **Subprogram Section (User-Defined Functions)** This optional section contains the definitions of user-defined functions that perform specific tasks and are called from the `main()` function or other functions in the program.

*EXAMPLE PROGRAM

*`/*
 * Documentation Section:
 * Simple C program to demonstrate the structure.
 */

#include <stdio.h> // Preprocessor Directive (Link Section)
#define PI 3.14    // Definition Section

int global_var = 10; // Global Declaration Section

// Function prototype (Global Declaration section)
void display_message();

int main() { // Main Function Section
    int local_var = 20; // Variable Declaration (local)
    printf("Global variable: %d\n", global_var); // Statement
    printf("Local variable: %d\n", local_var);   // Statement
    display_message(); // Function call
    return 0; // Return Statement
} // End of main()

void display_message() { // Subprogram Section (User-Defined Function)
    printf("This is a user-defined function.\n");
}
`
