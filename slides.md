---
theme: apple-basic

transition: fade-out
layout: intro
fonts:
  sans: FiraCode Nerd Font Mono
  serif: FiraCode Nerd Font Mono
  mono: FiraCode Nerd Font Mono
  provider: none
  fallbacks: false
---

# C Overview

Session 2

---
transition: fade-out
---

# Printing Literals

````md magic-move
//step one
```c {*|4}
#include <stdio.h>

int main() {
  printf("Hello, World!\n"); // output: Hello, World!
  return 0;
}
```

//step 2
```c {4}
#include <stdio.h>

int main() {
  printf("Aurka\n"); // output: Aurka
  return 0;
}
```

//step 3
```c {4}
#include <stdio.h>

int main() {
  printf("10\n"); // output: 10
  return 0;
}
```
````

---
transition: slide-up
---

# Printing with arguments

````md magic-move
//step 1
```c {4}
#include <stdio.h>

int main() {
  printf("%d\n", 10); // output: 10
  return 0;
}
```
````

---
transition: slide-up
---

# Creating a Simple Calculator

````md magic-move
//just sum
```c {4}
#include <stdio.h>

int main() {
  printf("%d\n", 10 + 5); // output: 15
  return 0;
}
```

//before all arithmetic operations
```c {4-7}
#include <stdio.h>

int main() {
  printf("%d\n", 10 + 5); // output: 15
  printf("%d\n", 10 + 5); // output: 15
  printf("%d\n", 10 + 5); // output: 15
  printf("%d\n", 10 + 5); // output: 15
  return 0;
}
```

//all arithmetic operations
```c {4-7}
#include <stdio.h>

int main() {
  printf("%d\n", 10 + 5); // output: 15
  printf("%d\n", 10 - 5); // output: 5
  printf("%d\n", 10 * 5); // output: 50
  printf("%d\n", 10 / 5); // output: 2
  return 0;
}
```
````

---
transition: slide-up
---

# Operators

- Arithmetic Operators: `+`, `-`, `*`, `/`, `%`
- Relational Operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Logical Operators: `&&`, `||`, `!`
- Bitwise Operators: `&`, `|`, `^`, `~`, `<<`, `>>`
- Assignment Operators: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `^=`, `<<=`, `>>=`
- Increment/Decrement Operators: `++`, `--`
- Conditional Operator: `? :`
- Comma Operator: `,`
- Sizeof Operator: `sizeof`
- Pointer Operators: `&`, `*`

---
transition: slide-up
---

# Creating a Simple Calculator

````md magic-move
//all arithmetic operations
```c {4-7}
#include <stdio.h>

int main() {
  printf("%d\n", 10 + 5); // output: 15
  printf("%d\n", 10 - 5); // output: 5
  printf("%d\n", 10 * 5); // output: 50
  printf("%d\n", 10 / 5); // output: 2
  return 0;
}
```

```c {4-7}
#include <stdio.h>

int main() {
  printf("%d\n", 20 + 5); // output: 25
  printf("%d\n", 20 - 5); // output: 15
  printf("%d\n", 20 * 5); // output: 100
  printf("%d\n", 20 / 5); // output: 4
  return 0;
}
```
````

---
transition: slide-up
---

# Variables

<v-click>

````md magic-move

```c {4-7}
#include <stdio.h>

int main() {
  printf("%d\n", 20 + 5); // output: 25
  printf("%d\n", 20 - 5); // output: 15
  printf("%d\n", 20 * 5); // output: 100
  printf("%d\n", 20 / 5); // output: 4
  return 0;
}
```

```c {4|4-8}
#include <stdio.h>

int main() {
  int a = 20;
  printf("%d\n", 20 + 5); // output: 25
  printf("%d\n", 20 - 5); // output: 15
  printf("%d\n", 20 * 5); // output: 100
  printf("%d\n", 20 / 5); // output: 4
  return 0;
}
```

```c {4-8}
#include <stdio.h>

int main() {
  int a = 20;
  printf("%d\n", a + 5); // output: 25
  printf("%d\n", a - 5); // output: 15
  printf("%d\n", a * 5); // output: 100
  printf("%d\n", a / 5); // output: 4
  return 0;
}
```

```c {4-8}
#include <stdio.h>

int main() {
  int a = 30;
  printf("%d\n", a + 5); // output: 35
  printf("%d\n", a - 5); // output: 25
  printf("%d\n", a * 5); // output: 150
  printf("%d\n", a / 5); // output: 6
  return 0;
}
```
````

</v-click>


---
transition: slide-up
---

# Changing Variables Value

````md magic-move

```c {4-8}
#include <stdio.h>

int main() {
  int a = 30;
  printf("%d\n", a + 5); // output: 35
  printf("%d\n", a - 5); // output: 25
  printf("%d\n", a * 5); // output: 150
  printf("%d\n", a / 5); // output: 6
  return 0;
}
```

```c {4-10|7}
#include <stdio.h>

int main() {
  int a = 30;
  printf("%d\n", a + 5); // output: 35
  printf("%d\n", a - 5); // output: 25
  a = 40;
  printf("%d\n", a * 5); // output: 200
  printf("%d\n", a / 5); // output: 8
  return 0;
}
```

```c {4|4,5|4,6|4,7|7|7,8|7,9|*}
#include <stdio.h>

int main() {
  int a = 30;
  printf("%d\n", a + 5); // output: 35
  printf("%d\n", a - 5); // output: 25
  a = 40;
  printf("%d\n", a * 5); // output: 200
  printf("%d\n", a / 5); // output: 8
  return 0;
}
```
````

---
transition: slide-up
---

# Dive into Variables

````md magic-move

```c {4-10}
#include <stdio.h>

int main() {
  int a = 30;
  printf("%d\n", a + 5); // output: 35
  printf("%d\n", a - 5); // output: 25
  a = 40;
  printf("%d\n", a * 5); // output: 200
  printf("%d\n", a / 5); // output: 8
  return 0;
}
```

```c {4}
#include <stdio.h>

int main() {
  int a = 30;
  return 0;
}
```

```c {4-5|4}
#include <stdio.h>

int main() {
  int a;
  a = 30;
  return 0;
}
```

````

---
transition: slide-up
---

# Data Types

````md magic-move

```c {4}
#include <stdio.h>

int main() {
  int a; 
  return 0;
}
```

```c {4}
#include <stdio.h>

int main() {
  float a;
  return 0;
}
```

```c {4-10}
#include <stdio.h>

int main() {
  int a = 30;
  printf("%d\n", a + 5); // output: 35
  printf("%d\n", a - 5); // output: 25
  a = 40;
  printf("%d\n", a * 5); // output: 200
  printf("%d\n", a / 5); // output: 8
  return 0;
}
```

```c {4-10}
#include <stdio.h>

int main() {
  float a = 30.5;
  printf("%f\n", a + 5.0); // output: 35.5
  printf("%f\n", a - 5.0); // output: 25.5
  a = 40.0;
  printf("%f\n", a * 5.0); // output: 200.0
  printf("%f\n", a / 5.0); // output: 8.0
  return 0;
}
```

````

---
transition: slide-up
class: font-size-3
---

# Different Data Types

- Primitive Data Types
  - `int`
  - `float`
  - `double`
  - `char`
- Void Data Types
  - `void`

<v-click hide>

- Derived Data Types
  - `array`
  - `pointer`
  - `structure`
  - `union`
- Enumeration Data Types
  - `enum`

</v-click>

---
transition: slide-up
---

# what is %d and %f?

data type | format specifier
-|-
int | %d
float | %f
char | %c

<v-click>

We'll explore more data types in a future session.

</v-click>

---
transition: slide-up
---

# Taking Input from User

````md magic-move

```c {4-10|6|4|5|6|7|4-10}
#include <stdio.h>

int main() {
  int a;
  printf("Enter a number: ");
  scanf("%d", &a); // input: 10
  printf("You entered: %d\n", a); // output: You entered: 10
  return 0;
}
```

```c {4-10}
#include <stdio.h>

int main() {
  float a;
  printf("Enter a number: ");
  scanf("%f", &a); // input: 10.5
  printf("You entered: %f\n", a); // output: You entered: 10.500000
  return 0;
}
```

```c {4-10}
#include <stdio.h>

int main() {
  char a;
  printf("Enter a character: ");
  scanf("%c", &a); // input: A
  printf("You entered: %c\n", a); // output: You entered: A
  return 0;
}
```

````
---
transition: slide-up
---

# Final Calculator

````md magic-move

```c {4-10|4|5|6|7|8|9|10|4-10}
#include <stdio.h>

int main() {
  float a, b;
  printf("Enter two numbers: ");
  scanf("%f %f", &a, &b); // input: 10.5 5.5
  printf("Sum: %f\n", a + b); // output: Sum: 16.000000
  printf("Difference: %f\n", a - b); // output: Difference: 5.000000
  printf("Product: %f\n", a * b); // output: Product: 57.750000
  printf("Quotient: %f\n", a / b); // output: Quotient: 1.909091
  return 0;
}
```

````

---
transition: slide-up
layout: center
---

# Practice | Play | Learn

---
transition: slide-up
---

- write a program that takes 3 numbers as input and prints the average of those numbers.
- write a program that takes principal, time, and rate as user input and calculates the compound interest.
