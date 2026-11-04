# Q2 – Paging

## Objective
To understand paging as a memory-management technique and perform logical-to-physical address translation using a page table.

## Requirements Covered
- Explain external fragmentation using a diagram.
- Translate logical addresses into physical addresses.
- Calculate page-table sizes for 32-bit and 48-bit address spaces using 4 KB pages.
- Calculate effective memory-access time with and without TLB.
- Compare page sizes of 1 KB, 4 KB and 2 MB.
- Explain multi-level, hashed and inverted page tables.
- Explain memory protection and shared pages.
- Calculate internal fragmentation for 100 processes.
- Calculate effective access time for different TLB hit ratios.
- Identify the Linux page size and page faults.
- Test addresses at page boundaries.
- Compare conventional paging with inverted page tables.

## Program File
- `paging.c` – Performs logical-to-physical address translation using a page table.

## Compilation and Execution
```bash
gcc -std=c11 -Wall -Wextra paging.c -o paging
./paging
```

Change `PAGE_SIZE` from 1024 to 2048 to perform the second experiment.

## Linux Commands
```bash
getconf PAGESIZE
/usr/bin/time -v ./paging
```

## Experimental Investigation
The program translates logical addresses using page numbers, offsets and frame numbers. Invalid addresses and page faults are identified.

The page size, internal fragmentation and TLB access times are investigated using calculations and experimental results.

## Conclusion
Paging divides logical memory into fixed-size pages and physical memory into frames. It removes external fragmentation but may cause internal fragmentation. The suitable page size depends on memory usage, page-table overhead and access performance.
