
Assignment operators in C are ==used to assign values to variables==. The primary operator is the simple assignment operator `=`, while others are compound assignment operators that combine an operation with an assignment for more concise code. 

Simple Assignment Operator

The most common assignment operator is the equal sign (`=`). It assigns the value of the operand on the right to the variable on the left. 

- **Syntax:** `variable = expression;`
- **Example:** `int x = 10;` (assigns the value 10 to the integer variable `x`) 

Compound Assignment Operators

Compound assignment operators offer a shorthand for combining an arithmetic or bitwise operation with an assignment. The expression `a op= b` is generally equivalent to `a = a op b`. 

Common compound assignment operators include `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `^=`, `<<=`, and `>>=`. For example, `x += 3;` is equivalent to `x = x + 3;`. 

Key Concepts

In C, the left side of an assignment must be a modifiable l-value, such as a variable. Assignment operators have right-to-left associativity, enabling chained assignments like `a = b = c = 10;`. They also have low precedence, meaning the expression on the right is usually evaluated before the assignment occurs

|Operator|Name|Equivalent Expression|Example|
|---|---|---|---|
|**`+=`**|Addition Assignment|`a = a + b`|`x += 5;`|
|**`-=`**|Subtraction Assignment|`a = a - b`|`x -= 2;`|
|**`*=`**|Multiplication Assignment|`a = a * b`|`x *= 3;`|
|**`/=`**|Division Assignment|`a = a / b`|`x /= 2;`|
|**`%=`**|Modulus Assignment|`a = a % b`|`x %= 3;`|
|**`&=`**|Bitwise AND Assignment|`a = a & b`|`x &= 1;`|
|**`|=`**|Bitwise OR Assignment|`a = a \| b`|
|**`^=`**|Bitwise XOR Assignment|`a = a ^ b`|`x ^= 1;`|
|**`<<=`**|Left Shift Assignment|`a = a << b`|`x <<= 2;`|
|**`>>=`**|Right Shift Assignment|`a = a >> b`|`x >>= 2;`|

Key Properties

- **Associativity:** Assignment operators follow **right-to-left** associativity. This allows "chaining," where a single value can be assigned to multiple variables: `a = b = c = 10;`.
- **Precedence:** They have very **low precedence** (usually lower than arithmetic, relational, and logical operators), meaning the right-side expression is evaluated completely before the assignment occurs.
- **Data Types:** The value on the right must be compatible with the data type of the variable on the left, or the compiler will perform an implicit type conversion.
- **L-values vs. R-values:** The left operand must be a "modifiable l-value" (something that can hold a value, like a variable), while the right operand can be any "r-value" (a constant, literal, or expression).