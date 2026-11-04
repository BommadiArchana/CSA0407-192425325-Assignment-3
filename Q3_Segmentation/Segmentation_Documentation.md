# Q3 – Segmentation

## Objective
To study segmentation and perform address translation using segment tables containing base and limit values.

## Requirements Covered
- Translate segment and offset addresses.
- Check whether an offset exceeds the segment limit.
- Explain segmentation with paging using an Intel x86 diagram.
- Display Linux process memory segments using `/proc/PID/maps`.
- Explain the programmer's view of memory.
- Explain segment protection and sharing.
- Evaluate external fragmentation.
- Compare pure paging, pure segmentation and segmented paging.
- Translate eight addresses manually and verify using a program.
- Trigger and explain a segmentation fault.
- Calculate fragmentation after loading and removing 20 segments.
- Compare the sizes of memory-management tables.

## Program File
- `segmentation.c` – Performs segment address translation and limit checking.

## Compilation and Execution
```bash
gcc -std=c11 -Wall -Wextra segmentation.c -o segmentation
./segmentation
```

## Linux Commands
```bash
cat /proc/PID/maps
```

Replace `PID` with the actual process ID.

## Experimental Investigation
Eight segment-offset combinations are tested. Valid addresses are translated using the base address, while invalid offsets are rejected.

A separate experiment is performed to generate a segmentation fault and examine process memory mappings.

## Conclusion
Segmentation divides a program into logical units such as code, data and stack. It supports logical memory organization, protection and sharing, but may cause external fragmentation. Modern operating systems primarily rely on paging for practical memory management.
