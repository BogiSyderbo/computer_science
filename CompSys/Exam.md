# Subjects
- Caching
- Virtual addressing

# Questions
## Caching
### 1
**Question**:
A computer uses 32-bit byte addressing. The computer uses a 2-way associative cache with a capacity of 32KB. Each cache block contains 16 bytes. Calculate the number of bits in the *TAG*, *SET*, and *OFFSET* fields of a main memory address.

**Solution**:
Since there are 16 bytes in a cache block, the *OFFSET* field must contain 4 bits ($2^4=16$). To determine the number of bits in the *SET* field, we need to determine the number of sets. Each set contains 2 cache blocks (2-way associative) so a set contains 32 bytes. There are 32KB bytes in the entire cache, so there are 32KB/32B = 1K sets.

Thus the set field contains 10 bits (210 = 1K).

Finally, the *TAG* field contains the remaining 18 bits (32 - 4 - 10). Thus a main memory address is decomposed as shown below.

![[Pasted image 20230927110717.png]]

![[2023.09.25#5.1]]

## Virtual addressing
![[2023.10.02#Exercises notes]]

