# Virtualisation
## Virtual address translation to physical


**Exam 2022-2023**
![[Pasted image 20240111210817.png]]
![[Pasted image 20240111212214.png]]

## Concurrency
*Concurrency* is the ability of a program to execute concurrent units in parallel. This improves the execution speed of a program.
### Multi-threaded programs
Programs that run concurrently on multiple threads are called *multi-threaded* programs.

You can think of a *thread* as a function running within the same memory space as other functions.

Each *thread* has its own *call stack* and *local variables* but they all share the same global memory address.

In **C**, you can create programs that create multiple threads using the function:
```C
Phtread_create()
```
This function creates two *threads*.
#### Example 1
```C
#include <stdio.h>
#include <stdlib.h>
#include "common.h"
#include "common_threads.h"
volatile int counter = 0;
int loops;

void *worker(void *arg) {
	int i;
	for (i = 0; i < loops; i++) {
		counter++;
	}
	return NULL;
}
int main(int argc, char *argv[]) {
	if (argc != 2) {
		fprintf(stderr, "usage: threads <value>\n");
		exit(1);
}
	loops = atoi(argv[1]);
	pthread_t p1, p2;
	printf("Initial value : %d\n", counter);
	Pthread_create(&p1, NULL, worker, NULL);
	Pthread_create(&p2, NULL, worker, NULL);
	Pthread_join(p1, NULL);
	Pthread_join(p2, NULL);
	printf("Final value
	: %d\n", counter);
	return 0;
}
```

### Persistence
**Persistent storage** is data that is stored such that it is not lost when a system crashes or is switched off. **DRAM** stores values in a *volatile* manner, such that data can be easily lost.

**Persistent storage** is usually stored in *HDDs* / *SSDs*.

The software in an **OS** that manages the disk is called the *file system*. 

**System calls** are routed to the *file system* when a file needs to be *read*, *written to*, created or deleted.
### Policies

### Processes
The **OS** creates an *illusion* of running many *programs* at the same time by *virtualising* the CPU. This is achieved creating many *processes* that seem to run at once. In reality, one process is running at once, where one process is stopped while another runs.

The technique of creating the *illusion* of having many **virtual CPUs** is known as *time sharing* of the CPU. By allowing the resource to be used for a little while by one entity, and then a little while by another, and so forth, the resource in question (e.g., the CPU, or a network link) can be shared by many.

Each process runs slowed when running *concurrently* instead of running a single process *sequentially*. *Time sharing* allows for the sharing of resources.

The counterpart of *time sharing* is *space sharing* where a resource is divided (in space) among those who wish to use it. For example, disk space is naturally a space-shared resource; once a block is assigned to a file, it is normally not assigned to another file until the user deletes the original file.