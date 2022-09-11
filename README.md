# Learn java
A guide for java.

## Comment in Java
```java
// this is single line comment
/* this is
multi line
comment */
```
## Create Variables in Java
```c
DataType VariableName = Value;

// Integer
int speedLimit = 80;
// Boolean
boolean flag = true | false;
// Floating-point
float myFloat = 3.4;
// Double
double myDouble = 3.4000;
// Character
char letter = 'a';
// String
String str = "Java Programming";
```

## Java Data Types
#### Primitive
| Data Type | Size | Range | Default value |
|:---:|:----:|:----:|:---:|
| `boolean` | 1 bite | (`true` or `false`) | `false`|
| `byte` | 8 bit | (`-128 to 127`) |`0`|
| `short` | 16 bit | (`-32768 to 32767`) |`0`|
| `int` | 32 bit | (`-2^31 to 2^31 - 1`) |`0`|
| `long` | 64 bit | (`-2^63 to 2^63 - 1`) |`0`|
| `double` | 64 bit(floating point) | (`-2^63 to 2^63-1`) |`0.0`|
| `float` | 32 bit(floating point) | (`-2^31 to 2^31 - 1`) |`0.0f`|
| `char` | 16 bit | (`'\u0000' to '\uffff'`) |`'\u0000'`|

###  Non Primitive
| Data Type | Size | Range | Default value |
|:---:|:----:|:----:|:---:|
| `String` | 16 bite * no of `char` | . | `'\u0000'`|

## Java Operators
### Arithmetic Operators
| Operator | Operation |
|:---:|:---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Modulo Operation (Remainder after division) |
| `/` | Division |

### Assignment Operators
| Operator | Example | Equivalent to |
|:---:|:---:|:---:|
| `=` | `a = b;` |`a = b;` |
| `+=` | `a += b;` | `a = a + b;` |
| `-=` | `a -= b;` | `a = a - b;` |
| `*=` | `a *= b;` | `a = a * b;` |
| `/=` | `a /= b;` | `a = a / b;` |
| `%=` | `a %= b;` | `a = a % b;` |

### Relational  Operators
| Operator | Description |
|:---:|:---|
| `==` | Is Equal To |
| `!=` | Not Equal To |
| `>` | Greater Than |
| `<` | Less Than |
| `>=` | Greater Than or Equal To |
| `<=` | Less Than or Equal To |

### Logical Operators
| Operator | Example | Meaning |
|:---:|:---:|:---:|
| `&&` (Logical AND) | expression1 `&&` expression2 | `true` only if both expression1 and expression2 are `true` |
| `ll` (Logical OR) | expression1 `ll` expression2 | `true` only if both expression1 and expression2 are `true` |
| `!` (Logical NOT) | `!` expression | `true` if expression is `false` and vice versa |

### Unary Operators
| Operator | Description |
|:---:|:---|
| `++` | Increment operator: increments value by 1 |
| `--` | Decrement operator: decrements value by 1 |

### Bitwise Operators
| Operator | Description |
|:---:|:---|
| `~` | Bitwise Complement |
| `<<` | Left Shift |
| `>>` | Right Shift |
| `>>>` | Unsigned Right Shift |
| `&` | Bitwise AND |
| `^` | Bitwise exclusive OR |

### Ternary Operator
```c
variable = Expression ? expression1 : expression2
```

## Java Input and Output
### Output
```java
System.out.print("output a string"); // output a string
System.out.println("same as print but end with \n char"); // same as print but end with \n char
int var = 10;
// use + opreter to Concatenated to output values
System.out.println("output a variable " + var); // output a variable 10
System.out.printf("this is similar to c's printf %d", var); // this is similar to c's printf 10
```

## Java Input
```java
// first import 'java.util.Scanner' to use input in java
import java.util.Scanner;
// create an object of Scanner
Scanner input = new Scanner(System.in);

// take input from the user
int number = input.nextInt(); 
// int -> .nextInt()
// long -> .nextLong()
long long_number = input.nextLong();
// float -> .nextFloat()
float float_number = input.nextFloat();
// double -> .nextDouble()
double double_number = input.nextDouble();
// String -> .next()
String string_input = input.nect();
```
