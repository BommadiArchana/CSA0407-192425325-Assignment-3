# Q4 – Virtual Memory and Demand Paging

## Objective
To understand virtual memory and demand paging and investigate page faults, memory access patterns and copy-on-write.

## Requirements Covered
- Explain the steps involved in handling a page fault.
- Calculate effective access time for different page-fault rates.
- Explain copy-on-write and the `fork()` system call.
- Explain thrashing and the working-set model.
- Explain how demand paging allows a 24 GB program to run with 16 GB RAM.
- Evaluate the maximum acceptable page-fault rate for a 10% slowdown.
- Explain equal and proportional frame allocation.
- Explain how the operating system detects and controls thrashing.
- Perform sequential and random memory-access experiments.
- Measure execution time as memory usage increases.
- Demonstrate copy-on-write using `fork()`.
- Plot page faults against the number of frames.

## Program File
- `virtual_memory.c` – Demonstrates memory allocation and sequential and random memory-access simulation.

## Compilation and Execution
```bash
gcc -std=c11 -Wall -Wextra virtual_memory.c -o virtual_memory
./virtual_memory
```

## Experimental Investigation
The program accesses allocated memory sequentially and randomly and records simulated first-access page faults.

Additional Linux experiments are required to measure actual page faults, memory usage and copy-on-write behaviour.

## Conclusion
Virtual memory allows programs to use an address space larger than the available physical RAM. Demand paging loads pages when they are required. Efficient memory access and good locality help reduce page faults and prevent thrashing.
