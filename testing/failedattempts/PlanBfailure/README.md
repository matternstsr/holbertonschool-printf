![image](https://github.com/matternstsr/holbertonschool-printf/assets/132416663/ce03e6b8-3b1e-4272-b8bb-e69bd775630a)
# Our amazing printf() function

**_printf** - formatted output conversion

**#include "main.h"** **int _printf(const char** *format* **, ...);**

*  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *

**Description**

The **_printf()** function produce output according to a *format* as described below. Also, write output to *stdout*, the standard output stream.

The **_printf()** function write the output under the control of a format string that specifies how subsequent arguments (or arguments accessed via the variable-length argument facilities of ***stdarg(3)\*** are converted for output.

*  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *

**Conversion specifiers**

A character that specifies the type of conversion to be applied. The conversion specifiers and their meaning are:

- **d, i**: The int\ argument should be signed decimal notation, and the resulting number is written.
- **c**: The int\ argument is converted to a char, and the resulting character is written.
- **s**: The const char\ argument is expected to be a pointer to an array of character type (pointer to a string).     Characters from the array are written up to (but not including) a terminating null byte ('\0').
- **%**: A '**%**' is written. No argument is converted. The complete conversion specification is '**%%**'.

*  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *

**Formatting of the format string**

The format string is a character string, beginning and ending inits initial shift state, if any. The format string is composed of zero or more directives: ordinary characters (not %), which are copied unchanged to the output stream; and conversion specifications, each of which results in fetching zero or more subsequent arguments. Each conversion specification is introduced by the character % and ends with conversion specifier.

*  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *

**About our chosen functions**

* **int _write(char c)**
  This function gets a char parameter and writes the parameter to the stdout, the standard output stream.

* ***int _print_char (va_list args)***
  This function gets a variadic arguments list, traverse the list, prints each character of char type and returns the length of the character.

* ***int _print_string (va_list args)***
This function gets a variadic arguments list, traverse the list, prints each string and returns the length of the string.

* **int _print_integer (va_list args)**
This function gets a variadic arguments list, traverse the list, prints each number of int type and returns the length of the integer.

* **int _our_formats (const char \*format, va_list args)**
This function gets a format to be printed and a variadic arguments list, next to check if the format is valid or invalid and according with the verification the resulting output is written to the standard output stream and returns the format length.

* **int _printspec (char format, va_list args):**
This function gets a format valid to be printed and a variadic arguments list to find the format in the list and selects the appropriate function to execute and writes the format to the standard output stream and returns the length of the valid format.

* **int _badspec (char prev_format, char format, int count)**
This function gets the previous format of the current format, the actual format and the current count of printed characters. Next, the invalid format is written to the standard output stream and returns the length of the invalid format.

* **void _integer_printer(int a)**
This function gets an integer and prints the last digit of the number as recursion is applied.

* **int _charchecker(char _type)**
Gets a type and checks if the passed parameter is present in a structure of valid conversion specifiers. Next, returns if the parameter is valid or invalid.

* **Return Value**
If not errors, the **_printf()** function return the number of characters printed (excluding the null byte used to end output to strings. If an output error is encountered, a negative value is returned.

*  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *  *

* **Examples**

_printf("I love holberton"); **// the output will be: I love Holberton**

_printf("%c", 'H'); // **the output will be: H**

_printf("Complete the sentence: Holberton %s rocks.\n", "totally"); **// the output will be: Complete the sentence: Holberton totally rocks.**

_printf("% s", "Holbies"); **// the output will be: Holbies**

_printf("% h"); **// the output will be: % h**

_printf("%!\n"); **// the output will be '%!'**

_printf("%s", "Holberton is awesome"); **// the output will be: Holberton is awesome**

**Created by**

**_printf()** (often confused with printf()) is written and maintained by Matt Ernst and Connor True.

