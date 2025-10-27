# ft_printf

A custom implementation of the standard C library's `printf` function, built as part of the 42 School curriculum.

## 📝 Description

This project recreates the behavior of the well-known C library function `printf`. The function handles variable numbers of arguments and supports various format specifiers for different data types. This implementation provides a deep understanding of variadic functions and formatted output in C.

## 🚀 Features

The `ft_printf` function supports the following format specifiers:

- `%c` - Character
- `%s` - String
- `%p` - Pointer address in hexadecimal format
- `%d` - Decimal (base 10) number
- `%i` - Integer in base 10
- `%u` - Unsigned decimal (base 10) number
- `%x` - Number in hexadecimal (base 16) lowercase format
- `%X` - Number in hexadecimal (base 16) uppercase format
- `%%` - Literal percent sign

## 📁 Project Structure

```
.
├── ft_printf.c          # Main printf function implementation
├── ft_printf.h          # Header file with function prototypes
├── ft_printf_bigx.c     # Handles %X format specifier
├── ft_printf_c.c        # Handles %c format specifier
├── ft_printf_d.c        # Handles %d and %i format specifiers
├── ft_printf_p.c        # Handles %p format specifier
├── ft_printf_s.c        # Handles %s format specifier
├── ft_printf_u.c        # Handles %u format specifier
├── ft_printf_x.c        # Handles %x format specifier
├── ft_putnbr_base.c     # Utility function for number base conversion
├── ft_putnbr_unsigned.c # Utility function for unsigned numbers
├── ft_putptr.c          # Utility function for pointer formatting
├── Makefile             # Build configuration
├── libft/               # Custom C library (dependency)
└── includes/            # Header files directory
```

## 🛠️ Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd printf
```

2. Compile the library:
```bash
make
```

This will create `libftprintf.a` library file.

## 💻 Usage

### Basic Usage

Include the header file and link the library:

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello, %s!\n", "World");
    ft_printf("Number: %d\n", 42);
    ft_printf("Hex: %x\n", 255);
    ft_printf("Pointer: %p\n", &main);
    return (0);
}
```

### Compilation

Compile your program with the library:

```bash
gcc your_program.c -L. -lftprintf -o your_program
```

## 🧪 Testing

The function returns the number of characters printed, just like the standard `printf`. You can test various format specifiers:

```c
#include "ft_printf.h"

int main(void)
{
    int len;

    len = ft_printf("Testing ft_printf:\n");
    len += ft_printf("Character: %c\n", 'A');
    len += ft_printf("String: %s\n", "Hello World");
    len += ft_printf("Integer: %d\n", -42);
    len += ft_printf("Unsigned: %u\n", 42u);
    len += ft_printf("Hex lower: %x\n", 255);
    len += ft_printf("Hex upper: %X\n", 255);
    len += ft_printf("Percent: %%\n");

    ft_printf("Total characters printed: %d\n", len);
    return (0);
}
```

## 📋 Requirements

- **Compiler**: GCC or Clang with C99 standard
- **Dependencies**: Custom libft library (included)
- **System**: Unix-like systems (Linux, macOS)

## 🔧 Makefile Rules

- `make` or `make all` - Compile the library
- `make clean` - Remove object files
- `make fclean` - Remove object files and the library
- `make re` - Recompile everything from scratch

## 🏗️ Implementation Details

The project uses:
- **Variadic functions** (`va_list`, `va_start`, `va_arg`, `va_end`)
- **Modular design** with separate functions for each format specifier
- **Base conversion algorithms** for hexadecimal and decimal representations
- **Memory-safe string handling**

## ⚡ Performance

The implementation focuses on:
- Efficient character-by-character output
- Minimal memory allocation
- Clean separation of concerns
- Compliance with 42 School coding standards (Norminette)

## 📚 Learning Objectives

This project helps understand:
- Variadic functions in C
- Format specifier parsing
- Number base conversion
- Memory management
- Modular programming design
- Library creation and linking

## 👨‍💻 Author

**fli** - 42 School Student
- GitHub: [@itsfwenk](https://github.com/itsfwenk)

## 📄 License

This project is part of the 42 School curriculum and follows the school's academic guidelines.

---

*Note: This implementation is designed for educational purposes as part of the 42 School curriculum.*
