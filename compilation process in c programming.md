The compilation process in C is ==the multi-stage system of converting human-readable source code into machine-executable binary code==. This process involves four main phases: **preprocessing**, **compilation**, **assembly**, and **linking**. 

The Four Phases of C Compilation 

A C program, typically saved as a `.c` file, goes through the following transformations: 

1. Preprocessing

This is the initial phase where the preprocessor program prepares the source code for the actual compiler. It handles all lines beginning with the `#` symbol (preprocessor directives). 

- **Removal of Comments:** All comments (`//` and `/* */`) are stripped from the code.
- **File Inclusion:** The preprocessor replaces `#include` directives with the actual content of the specified header files (e.g., `stdio.h`).
- **Macro Expansion:** Macros defined with `#define` are replaced with their corresponding values or expressions throughout the code.
- **Conditional Compilation:** Directives like `#ifdef` or `#ifndef` determine which blocks of code should be included or excluded before compilation. 

The output of this stage is an expanded source code file, typically with a `.i` extension. 

2. Compilation

The preprocessed code (the `.i` file) is then passed to the compiler. This stage involves complex analysis to check for syntax and semantic errors and translates the code into assembly language. 

- **Error Checking:** The compiler parses the code (lexical and syntax analysis) and reports any errors.
- **Optimization:** The compiler may apply various techniques to make the resulting assembly code more efficient. 

The output of this stage is an assembly code file, typically with a `.s` extension. 

3. Assembly

The assembler takes the assembly language code (`.s` file) as input and converts it into machine-level code (binary instructions, or 1s and 0s) that the computer's processor can understand. 

The output is an object file, typically with a `.o` (Unix/Linux) or `.obj` (Windows) extension. This file contains machine code for the functions and variables in that specific source file but cannot be run on its own because function calls from other files or libraries are not yet resolved. 

4. Linking

This is the final stage where the linker combines all the object files from different modules or source files, along with necessary external library files (which contain definitions for standard functions like `printf()` or `scanf()`), to produce a single, final executable file. 

- **Symbol Resolution:** The linker resolves all the "holes" or undefined references to functions and variables that were left during the assembly stage by finding their definitions in other object files or libraries.
- **Relocation:** It organizes the code and data into a final memory layout. 

The final output is an executable file, commonly named `a.out` on Linux systems or `program.exe` on Windows. This file can then be loaded into memory and executed by the operating system. 

A popular compiler suite used for this entire process is the GNU Compiler Collection (GCC).