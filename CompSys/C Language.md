# Introduction
## Setup
### Recommended compiler flags
```
gcc -Wall -Wextra -pedantic -std=c11 -c [file]
```
- *Wall* Turns on (almost) all warnings
- *Wextra* Add warnings for unassigned values and more
- *pedantic* Makes warnings if you goes outside ISO C
- *std=c11* Chooses the latest C standard
### Makefile
```
CC=gcc
CFLAGS=-std=c11 -Wall -Werror -Wextra -pedantic
.PHONY: clean all
cmd: updatedfile(s).c
$(CC) $(CFLAGS) -o $@ -c $<
```
### Style guide
Opening braces should be on the same line as the declaration:
```
int f() {
  for (int i = 0; i < 100; i++) {
    if (i % 2 == 0) {
      // Do something.
    }
  }
  // Return something.
}
```
- Use 2 spaces for indentation, indent when entering a new scope
- All functions must return a value, returning void is not allowed
- Code must be warning-free
	- Use booleans rather than 0 and 1
## Grammar

**Special words** are concepts and features that the C language imposes and cannot be changed. For example: $\texttt{\#include, int, void}$

### Punctuation
- *Brackets*: $\{\cdots\},(\cdots),[\cdots],/*\cdots*/ \text{, and } <\cdots>$
- *Separators* or *terminators*: comma and semicolon
- *Comments*, using the construct $/*\cdots*/$, which are ignored by the compiler
- *Literals*, such as $\texttt{0, 1, 3, 4, 5, 9.0, 2.9, 3.E+25, .00007}$.
- *Identifiers*: these are "names", for example $\texttt{main, printf, size\_t} \text{, and } \texttt{EXIT\_SUCCESS}$
	- Data objects, also referred to as variables
	- Type aliases
	- Functions
	- Constants
- *Operators*
	- = for initialization and assignment
	- < for comparison
	- ++ to increment a variable
	- * to multiply two values
### Declarations

### Statements
Statements are instructions that tell the compiler what to do with identifiers that have been declared so far.:
## Function examples
### Hello world!
```
#include <stdio.h>

int main() {
	printf("Hello, World!\n");
}
```

This is a program that contains a function $\texttt{main}$ that receives no arguments.  The function creates an executable file when compiled that prints the string $\texttt{Hello, World!}$ to the console.

By saving the program to a file $\texttt{hello.c}$ and running the command $\texttt{gcc -o hello hello.c}$ to compile the program the executable file $\texttt{hello}$ is created. The file can be run with the command $\texttt{./hello}$.

The first line of the tells the program to include information about the standard input/output library. 

### Add 
```
#include <stdio.h>

int main() {
	int x, y, sum;
	
	printf("Enter two integers: ");
	scanf("%d %d", &x, &y);

	sum = x + y;

	printf("%d + %d = %d \n", x, y, sum);
}

```

This program declares three integer variables: *x*, *y*, and *sum*. When the program is run, a string requesting two integers is printed to the terminal. The *scanf* function reads data from the standard input stream (the keyboard) and stores them in the variables *x* and *y*.  The sum is then declared with the *sum* variable as the sum of *x* and *y*.  Finally, the result of the sum is printed.



# Operators
## Arithmetic
![[Pasted image 20230905154946.png]]
## Object operators
![[Pasted image 20230905155022.png]]
## Type operators
![[Pasted image 20230905155035.png]]
## Logical operators
![[Pasted image 20230906094546.png]]
int isAscii(FILE *file){
	bool is_ascii = true;
	unsigned char c;
	for(size_t i = 0; fread(&c, sizeof(char), 1, file) == 1; i++) {
		if ((c > 31 && c < 127) == false){
			bool is_ascii = false;
		}
	}
	return is_ascii;
}
