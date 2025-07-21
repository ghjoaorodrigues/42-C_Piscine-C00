# C Piscine - C 00

![42 Badge](https://img.shields.io/badge/42-C_Piscine-brightgreen)
![C Badge](https://img.shields.io/badge/Language-C-blue)
![Status Badge](https://img.shields.io/badge/Status-Completed-success)

## What I Learned

Through this introductory module of the C Piscine at 42 School, I developed fundamental programming skills:

- **Basic I/O operations** - Learned to use the `write()` system call for character and string output
- **Function prototyping** - Understanding proper function declarations and implementations
- **ASCII manipulation** - Working with character values and ASCII arithmetic
- **Conditional logic** - Implementing decision-making structures in C
- **Loop constructs** - Using iterative approaches for repetitive tasks
- **Algorithm design** - Breaking down complex problems into smaller, manageable pieces
- **Edge case handling** - Considering boundary conditions and special cases
- **Code organization** - Writing clean, readable functions that follow a single responsibility
- **Debugging skills** - Testing functions thoroughly and identifying logical errors
- **Norminette compliance** - Following 42's strict coding standards from day one

This foundational module established my understanding of C programming basics and problem-solving methodologies essential for all subsequent projects.

## About the Project

C 00 is the first module of the intensive C Piscine at 42 School. It introduces students to basic C programming concepts through a series of progressively challenging exercises that focus on:

- Character and string manipulation
- Basic mathematical operations
- Pattern recognition and generation
- Recursive thinking
- Code optimization

## Implementation Details

The module consists of 9 exercises (ex00-ex08) that build upon each other:

### Basic Output Functions

Foundation exercises focusing on character and string display:

| Exercise | Function | Description |
|----------|----------|-------------|
| ex00 | ft_putchar | Display a single character using write() |
| ex01 | ft_print_alphabet | Print lowercase alphabet a-z |
| ex02 | ft_print_reverse_alphabet | Print lowercase alphabet z-a |
| ex03 | ft_print_numbers | Print digits 0-9 |

### Conditional Logic

Introduction to decision-making in C:

| Exercise | Function | Description |
|----------|----------|-------------|
| ex04 | ft_is_negative | Display 'N' for negative numbers, 'P' for positive/zero |

### Complex Algorithms

Advanced exercises requiring mathematical thinking:

| Exercise | Function | Description |
|----------|----------|-------------|
| ex05 | ft_print_comb | Print all 3-digit combinations (012, 013, ..., 789) |
| ex06 | ft_print_comb2 | Print all 2-number combinations (00 01, 00 02, ..., 98 99) |
| ex07 | ft_putnbr | Display any integer value within int range |
| ex08 | ft_print_combn | Print all n-digit combinations (recursive approach) |

## Usage

Each exercise should be compiled and tested individually:

```bash
# Compile a specific exercise
cc -Wall -Wextra -Werror ft_putchar.c

# Test with a main function (if required)
cc -Wall -Wextra -Werror main.c ft_putchar.c -o test
./test
```

## Code Examples

### Basic Character Output (ex00)
```c
void ft_putchar(char c)
{
    write(1, &c, 1);
}
```

### Alphabet Display (ex01)
```c
void ft_print_alphabet(void)
{
    char c = 'a';
    while (c <= 'z')
    {
        write(1, &c, 1);
        c++;
    }
}
```

### Number Display (ex07)
```c
void ft_putnbr(int nb)
{
    if (nb == -2147483648)
    {
        write(1, "-2147483648", 11);
        return;
    }
    if (nb < 0)
    {
        write(1, "-", 1);
        nb = -nb;
    }
    if (nb >= 10)
        ft_putnbr(nb / 10);
    char digit = nb % 10 + '0';
    write(1, &digit, 1);
}
```

## Technical Challenges Overcome

- **Understanding system calls** - Learning to use `write()` instead of higher-level functions like `printf()`
- **ASCII arithmetic** - Converting between characters and their numeric representations
- **Recursive algorithms** - Implementing functions that call themselves (especially in ex08)
- **Combination generation** - Developing logical patterns for generating unique combinations
- **Integer overflow handling** - Managing edge cases like `INT_MIN` in ft_putnbr
- **Memory constraints** - Working with limited function scope and no dynamic allocation
- **Output formatting** - Creating precise output formats without string manipulation functions

## Key Concepts Mastered

- **Iterative vs Recursive approaches** - Understanding when each method is most appropriate
- **Mathematical decomposition** - Breaking numbers into individual digits
- **Pattern recognition** - Identifying mathematical relationships in combination problems
- **Boundary testing** - Ensuring functions work correctly with edge cases
- **Code efficiency** - Writing optimal solutions within the constraints of basic C

---

*This project was completed as part of the 42 School C Piscine, demonstrating my foundational understanding of C programming, algorithmic thinking, and problem-solving skills essential for software development.*

---

## License

This project is licensed under the [MIT License](./LICENSE).
