_printf 📄
A formatted output conversion C program completed as part of the low-level programming and algorithm track at Holberton School. The program is a pseudo- recreation of the C standard library function, printf.

Dependencies 👫
The _printf function was coded on an Ubuntu 14.04 LTS machine with gcc version 4.8.4.

Usage 🏃
To use the _printf function, assuming the above dependencies have been installed, compile all .c files in the repository and include the header holberton.h with any main function.

Example main.c:

#include "holberton.h"

int main(void)
{
    _printf("Hello, World!");

    return (0);
}
Compilation:

$ gcc *.c -o tester
Output:

$ ./tester
Hello, World!
$
Description 💬
The function _printf writes output to standard output. The function writes under the control of a format string that specifies how subsequent arguments (accessed via the variable-length argument facilities of stdarg) are converted for output.

Prototype: int _printf(const char *format, ...);

Return Value
Upon successful return, _printf returns the number of characters printed (excluding the terminating null byte used to end output to strings). If an output error is encountered, the function returns -1.

Format of the Argument String
The format string argument is a constant character string composed of zero or more directives: ordinary characters (not %) which are copied unchanged to the output stream; and conversion specifications, each of which results in fetching zero or more subsequent arguments. Conversion specification is introduced by the character % and ends with a conversion specifier. In between the % character and conversion specifier, there may be (in order) zero or more flags, an optional minimum field width, an optional precision and an optional length modifier. The arguments must correspond with the conversion specifier, and are used in the order given.

Flag Characters
The character % may be followed by zero or more of the following flags:

For o conversions, the first character of the output string is prefixed with 0 if it was not zero already.
For x converions, 0x is prepended for non-zero numbers.
For X conversions, 0X is prepeneded for non-zero numbers.
Example main.c: