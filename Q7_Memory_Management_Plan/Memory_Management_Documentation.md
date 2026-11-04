# Q7 – Design a Memory-Management Plan from First Principles

## Objective
To design and evaluate a memory-management plan for a smart factory edge device with 2 GB RAM and no swap disk.

## Requirements Covered
- Identify memory requirements and timing constraints of the three tasks.
- Identify tasks that can and cannot tolerate page faults.
- Define measurable memory-management requirements.
- Compare contiguous allocation, paging, segmentation and demand paging.
- Explain memory locking using `mlock()`.
- Write a program to lock memory for a time-critical loop.
- Measure worst-case delay with and without memory locking.
- Simulate memory usage of the three tasks using a page-replacement simulator.
- Verify that the real-time task is not delayed.
- Justify the memory-management design using measurements.
- Evaluate the addition of a fourth task requiring 500 MB.
- Identify a remaining system limitation.
- Compare Linux with locked memory and an RTOS without virtual memory.

## Program File
- `memory_management.c` – Demonstrates memory locking, execution-delay measurement and FIFO page-replacement simulation.

## Compilation and Execution

Linux:
```bash
gcc -std=c11 -Wall -Wextra memory_management.c -o memory_management
./memory_management
```

Windows Dev-C++:
Compile and execute using the Dev-C++ compiler. The Windows version uses `VirtualLock()` instead of Linux `mlock()`.

## Experimental Investigation
The program measures execution delay with and without memory locking and performs a FIFO page-replacement simulation.

The results are used to discuss the memory requirements of the real-time control task, machine-learning task and logging task.

## Conclusion
A suitable memory-management plan should protect the time-critical control task from delays caused by page faults. Memory locking can help prevent selected memory pages from being paged out. The remaining memory must be allocated carefully to machine-learning and logging tasks while considering future expansion and system limitations.
