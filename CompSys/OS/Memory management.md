# Memory
*Physical memory* can be presented as an array of bytes. Each byte is assigned an *address* which needs to be specified when *reading* from or *writing* to memory. 

Memory stores *variables* and each *instruction* of a *program*. This means that memory is accessed for every *instruction fetch*.

## Memory allocation

### The heap
Memory requests are satisfied by allocating portions from a large pool of memory called *the heap*.
![[Pasted image 20240111163246.png]]

The heap consists of *blocks* stacked on top of each other. The blocks in this case have a *header* and *footer* which have identical contents.

The *header/footer* contains info about the size of the block and whether the previous and current block are allocated or free.



#### Exam 2020/21

- First place indicates the use of the current block (1 allocated, 0 free)
- Second place indicates the use of the previous block (1 allocated, 0 free)
- Third place is always unused and set to 0

0x13 = 0001 0011

Current block allocated
previous block allocated


Size is found by setting the last 3 bits to zero



Block size = 0001 0000 = 16

**free**

Current block = 0001 0011 = 0001 0010 = 0x12
Next block = 0001 0001 = 0x11

**realloc**

We need to round up to 16

Lowest header = 0010  0011 = 0x23

Footer of current block = 0010 0011 = 0x23

Top footer = 0001 0011