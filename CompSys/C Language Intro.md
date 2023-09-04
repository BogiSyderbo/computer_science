# Introduction
## Function examples

### Hello world!
```
#include <stdio.h>

main()
{
	printf("Hello, World!\n");
}
```

This is a program that contains a function $\texttt{main}$ that receives no arguments.  The function creates an executable file when compiled that prints the string $\texttt{Hello, World!}$ to the console.

By saving the program to a file $\texttt{hello.c}$ and running the command $\texttt{gcc -o hello hello.c}$ to compile the program the executable file $\texttt{hello}$ is created. The file can be run with the command $\texttt{./hello}$.

The first line of the tells the program to include information about the standard input/output library. 

### Add 
```
#include <stdio.h>

main()
{
	int x, y, sum;
	
	printf("Enter two integers: ");
	scanf("%d %d", &x, &y);

	sum = x + y;

	printf("%d + %d = %d \n", x, y, sum);
}

```

This program declares three integer variables: *x*, *y*, and *sum*. When the program is run, a string requesting two integers is printed to the terminal. The *scanf* function reads data from the standard input stream (the keyboard) and stores them in the variables *x* and *y*.  The sum is then declared with the *sum* variable as the sum of *x* and *y*.  Finally, the result of the sum is printed.

### Arrays
