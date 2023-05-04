# Libft
**Create your own library in C** - *12/04 - 27/04 (70 hours)*

## Overview

1. [Project description](#1-project-description)
2. [Instructions](#2-instructions)
3. [Content learned](#3-content-learned)
4. [Project](#4-project)
	- [About Libc](#about-libc)
	- [PART I](#part-i)
	- [PART II](#part-ii)
	- [BONUS](#bonus)
5. [Header](#5-header)
6. [Makefile](#6-makefile)
7. [How to use this Project](#7-how-to-use-this-project)
8. [Conclusion](#8-conclusion)
9. [Credits]()

### 1. Project description

This is my first project in the C programming language, which I am working on as part of my studies at 42 School. My goal is to create a library inspired by the **libc library** that is widely used in the C programming community. As I work through my C assignments, I will be updating the library to make it more comprehensive and complete.

This is an ongoing project and I understand that it will take time to complete, but I am committed to expanding the library throughout the year. To ensure that I am meeting the requirements of each assignment, I will be careful about what functions are allowed in each project.

I believe that this project will help me develop my C programming skills and provide me with a deeper understanding of how libraries work. Moreover, I hope that the library I create will be useful to other developers in the C programming community.

[return](#overview)

### 2. Instructions

>Technical considerations:
> - Declaring global variables is forbidden.
> - If you need helper functions to split a more complex function, define them as static functions. This way, their scope will be limited to the appropriate file.
> - Place all your files at the root of your repository.
> - Turning in unused files is forbidden.
> - Every .c files must compile with the flags -Wall -Wextra -Werror.
> - You must use the command ar to create your library. Using the libtool command is forbidden.
> - Your libft.a has to be created at the root of your repository.
> - It should not quit unexpectedly.
> - All memory allocation must be freed.
> - Submit a makefile!

[return](#overview)

### 3. Content learned

This section provides an overview of the content learned during this project, including headers, libraries, Makefile, and more.

- Headers
- Libraries
	- libc.h
	- ctype.h
	- string.h
	- stdlib.h
	- stddef.h
	- unistd.h
- Makefile
	- rules: $(NAME), all, clean, fclean and re
	- Variables
- Typecasting
- Static functions
- File descriptors
- Linked lists
	- typedef struct
	- 'restrict' qualifier

[return](#overview)

### 4. Project

#### About Libc

The standard C library, also known as "libc", is a collection of ready-made functions and tools that C programmers can use in their programs. These functions and tools are designed to provide basic functionality that is commonly used in C programming, such as input/output operations, string manipulation, memory management, and mathematical operations.

By using these pre-made functions, C programmers can write more efficient and portable code that can work across different systems and platforms. This means that they don't have to write everything from scratch, but can instead rely on the standard library to provide the tools they need.

In summary, the standard C library is a useful tool for C programmers that provides a set of standardized functions and tools to make programming easier and more efficient.

[return](#overview)

#### PART I

**All functions were tested with [francinette](https://github.com/xicodomingues/francinette).**

*ctype.h*

| Function   | Description													| Francinette		|
| ---------- | ------------------------------------------------------------ | ----------------- |
| ft_isalpha | Checks if the passed character is an alphabet or not.		| :heavy_check_mark:|
| ft_isdigit | Checks if the passed character is a digit or not.			| :heavy_check_mark:|
| ft_isalnum | Checks whether the given character is alphanumeric or not.	| :heavy_check_mark:|
| ft_isascii | Test whether c is a 7-bit US-ASCII character code.			| :heavy_check_mark:|
| ft_isprint | Checks whether a character is a printable character or not.	| :heavy_check_mark:|
| ft_toupper | Returns lowercase letter to an uppercase  letter.			| :heavy_check_mark:|
| ft_tolower | Returns uppercase letter to a lowercase  letter.				| :heavy_check_mark:|

*string.h*

| Function   | Description													| Francinette		|
| ---------- | ------------------------------------------------------------ | ----------------- |
| ft_strlen	 | Determines the length of a string excluding the ending null character. | :heavy_check_mark:|
| ft_memset	 | Fills the first n bytes of the memory area pointed to by s with the constant byte c. | :heavy_check_mark:|
| ft_bzero	 | Erases the data in the n bytes of the memory starting at the location pointed to by s. | :heavy_check_mark:|
| ft_memcpy	 | Copies n bytes from memory area src to memory area dest. | :heavy_check_mark:|
| ft_memmove | Copies n bytes from memory area src to memory area dest. | :heavy_check_mark:|
| ft_strlcpy | Copy a string from the source string to the destination string. | :heavy_check_mark:|
| ft_strlcat | Appends the NUL-terminated string src to the end of dst. | :heavy_check_mark:|
| ft_strchr	 | Returns a pointer to the first occurrence of the character c in the string s. | :heavy_check_mark:|
| ft_strrchr | Returns a pointer to the last occurrence of the character c in the string s. | :heavy_check_mark:|
| ft_strncmp | Compares only the first (at most) n bytes of s1 and s2. | :heavy_check_mark:|
| ft_memchr	 | Scans the initial n bytes of the memory area pointed to by s for the first instance of c. | :heavy_check_mark:|
| ft_memcmp	 | Compares the first n bytes of the memory areas s1 and s2. | :heavy_check_mark:|
| ft_strnstr | Locates the first occurrence of the string little in the string big. | :heavy_check_mark:|
| ft_strdup	 | Returns a pointer to a new string which is a duplicate of the string s. | :heavy_check_mark:|

*stdlib.h*

| Function   | Description													| Francinette		|
| ---------- | ------------------------------------------------------------ | ----------------- |
| ft_atoi	 | Converts a string pointed to by nptr to int.  | :heavy_check_mark:|
| ft_calloc  | Allocates memory for an array of nmemb elements of size bytes each and returns a pointer to the allocated memory. The memory is set to zero. | :heavy_check_mark:|

[return](#overview)

#### PART II

> Set of functions that are either not in the libc or that are part of it but in a different form.

| Function   | Description													| Francinette		|
| ---------- | ------------------------------------------------------------ | ----------------- |
| ft_substr | Allocates and returns a substring from the string ’s’. | :heavy_check_mark:|
| ft_strjoin | Allocates and returns a new string, which is the result of the concatenation of ’s1’ and ’s2’. | :heavy_check_mark:|
| ft_strtrim | Allocates and returns a copy of ’s1’ with the characters specified in ’set’ removed from the beginning and the end of the string. | :heavy_check_mark:|
| ft_split  | Allocates and returns an array of strings obtained by splitting ’s’ using the character ’c’ as a delimiter. | :heavy_check_mark:|
| ft_itoa | Allocates and returns a string representing the integer received as an argument. | :heavy_check_mark:|
| ft_strmapi | Applies the function ’f’ to each character of the string ’s’. | :heavy_check_mark:|
| ft_striteri | Applies the function ’f’ on each character of the string passed as argument, passing its index as first argument. | :heavy_check_mark:|
| ft_putchar_fd[¹] | Outputs the character ’c’ to the given file descriptor. | :heavy_check_mark:|
| ft_putstr_fd[¹] | Outputs the string ’s’ to the given file descriptor. | :heavy_check_mark:|
| ft_putendl_fd[¹] | Outputs the string ’s’ to the given file descriptor followed by a newline. | :heavy_check_mark:|
| ft_putnbr_fd[¹] | Outputs the integer ’n’ to the given file descriptor. | :heavy_check_mark:|

> [¹]: A file descriptor is an integer value that represents an open file or input/output device within the operating system. This value is assigned by the operating system when a file or device is opened, and it uniquely identifies the file or device within the program. The integer value of a file descriptor represents an index into a table maintained by the operating system, called the file descriptor table. This table contains information about all of the open files and devices being used by the program. 0 is a special file descriptor that represents standard input, also known as stdin. Standard input is typically connected to the keyboard or another input device, and is used to read input from the user. 1 is a special file descriptor that represents standard output, also known as stdout. Standard output is typically connected to the console or another output device, and is used to display output from the program. 2 is a special file descriptor that represents standard error, also known as stderr. Standard error is typically connected to the console or another output device, and is used to display error messages and other diagnostic information from the program. File descriptors with values greater than or equal to 3 represent open files and devices that are being used by the program. The specific values of these descriptors are assigned by the operating system, and are typically unique to each open file or device. In summary, file descriptors are integer values that uniquely identify open files and input/output devices within the program, and allow the program to interact with the operating system's file table to read and write data. - [chatgpt](https://chat.openai.com/)

[return](#overview)

#### BONUS

> Set of functions that will make the use of lists easy.

| Function   | Description													| Francinette		|
| ---------- | ------------------------------------------------------------ | ----------------- |
| ft_lstnew | Allocates and returns a new node. | :heavy_check_mark:|
| ft_lstadd_front | Adds the node ’new’ at the beginning of the list. | :heavy_check_mark:|
| ft_lstsize | Counts the number of nodes in a list. | :heavy_check_mark:|
| ft_lstlast | Returns the last node of the list. | :heavy_check_mark:|
| ft_lstadd_back | Adds the node ’new’ at the end of the list. | :heavy_check_mark:|
| ft_lstdelone | Takes as a parameter a node and frees the memory of the node’s content	using the function ’del’ given as a parameter and free the node. | :heavy_check_mark:|
| ft_lstclear | Deletes and frees the given node and every successor of that node, using the function ’del’ and free. | :heavy_check_mark:|
| ft_lstiter | Iterates the list ’lst’ and applies the function ’f’ on the content of each node. | :heavy_check_mark:|
| ft_lstmap | Iterates the list ’lst’ and applies the function ’f’ on the content of each node. Creates a new list resulting of the successive applications of the function ’f’. | :heavy_check_mark:|

[return](#overview)

### 5. Header

Header files are a way to declare functions, constants, and other declarations that are used by multiple source code files. They help to separate interface and implementation details, make code easier to read and maintain, and enable the creation of reusable libraries.

This library includes functions to manipulate strings, check characters, convert data types, and work with linked lists. It can be used as a replacement for or in addition to the standard C library functions.

[return](#overview)

### 6. Makefile

A Makefile is a special file that contains a set of directives used to build and manage the project. In this Makefile, I defined the compiler, compiler flags, source files, object files, and the name of the library archive that were created.

| Variables   | Description													|
| ----------- | ------------------------------------------------------------ |
| CC | The compiler to be used for compiling the source code. |
| LIB_CMD | The command used to create the static library archive. |
| NAME | The name of the library archive that will be created. |
| CFLAGS | The compiler flags to be used while compiling the source code. |
| SRC | A list of source files used in the project. |
| OBJ | A list of object files created by compiling the source files.|
| BSRC | A list of bonus source files used in the project. |
| BOBJ | A list of bonus object files created by compiling the bonus source files. |

| Rules	     | Description													|
| ---------- | ------------------------------------------------------------ |
| %.o: %.c | Specifies how to compile a C source file into an object file. The "$^" variable refers to the name of the prerequisite and the "$@" variable refers to the name of the target |
| "$(NAME)" | Specifies how to create the static library archive. |
| all | Specifies that the default target for the Makefile is to build the library archive specified in the $(NAME) rule. |
| bonus | Specifies how to build the bonus part of the project. |
| clean | Specifies how to remove all the object files generated during compilation. |
| fclean | Specifies how to remove all the object files and the library archive generated during compilation. |
| re | Specifies how to rebuild the entire project from scratch by removing all the generated files and rebuilding them again. |

[return](#overview)

### 7. How to use this Project

To use the functions in the library, add these files to your project's directory, include the **libft.h** header file in your C source code. You can compile the library by running **make**.

	#include "libft.h"

[return](#overview)

### 8. Conclusion

In conclusion, the libft project was a great learning opportunity for me. I improved my programming skills and gained a better understanding of the C programming language by implementing various functions that are commonly used in programming.

This project taught me the importance of writing organized and reusable code, which will save me time in future projects. I also learned the importance of testing my code thoroughly to ensure it works correctly.

Overall, the libft project was a challenging but rewarding experience that helped me develop my programming skills. I'm excited to use what I've learned in future projects.

[return](#overview)
