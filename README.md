# 🖨️ ft_printf – 42 Project

## 📖 Description

**ft_printf** is a reimplementation of the standard C function printf, developed as part of the 42 curriculum.

The objective is to recreate the behavior of `printf`, handling formatted output and a variety of conversion specifiers, while managing variable arguments.

This project introduces:

* Variadic functions using `va_list`
* Format string parsing
* Type conversion and formatting
* Low-level output handling (typically using `write`)

---

## ⚙️ Instructions

### 🛠️ Compilation

Clone the repository and compile the project:

```bash id="u1h8kp"
git clone git@github.com:JoaodMesquita/printf.git
cd ft_printf
make
```

This will generate:

* `libftprintf.a` (static library)

---

### 🚀 Usage

### 📌 Function Prototype

```c id="7azc2m"
int ft_printf(const char *format, ...);
```

### ▶️ Example

```c id="c4x9qd"
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello %s!\n", "world");
    ft_printf("Number: %d\n", 42);
    ft_printf("Hex: %x\n", 255);
    return (0);
}
```

---

## 🔄 Supported Conversions

* `%c` – character
* `%s` – string
* `%p` – pointer
* `%d` / `%i` – signed integers
* `%u` – unsigned integers
* `%x` / `%X` – hexadecimal
* `%%` – percent sign

---

## 🔄 How It Works

1. The function parses the format string character by character.
2. When a `%` is found, it identifies the conversion specifier.
3. Arguments are retrieved using `va_arg`.
4. Each type is formatted accordingly and written to the output.
5. The function returns the total number of printed characters.

---

## 📚 Resources

### Variadic Functions

* `man stdarg`
* https://en.wikipedia.org/wiki/Variadic_function

### Standard printf Behavior

* `man 3 printf`

### Number Conversions

* https://www.geeksforgeeks.org/convert-decimal-to-hexadecimal-in-c/

### Debugging Tools

* `valgrind`
* `gdb`

---
