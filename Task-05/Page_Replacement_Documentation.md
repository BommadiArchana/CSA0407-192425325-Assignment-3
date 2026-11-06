# Q5 – Page-Replacement Techniques

## Objective
To implement and compare FIFO, LRU and Optimal page-replacement algorithms and evaluate their page-fault performance.

## Requirements Covered
- Implement FIFO, LRU and Optimal algorithms.
- Count page faults using 3 and 4 frames.
- Demonstrate Belady's Anomaly using FIFO.
- Explain the Clock (Second-Chance) algorithm.
- Explain why Optimal is theoretically the best algorithm.
- Explain the stack property of LRU.
- Evaluate hardware support required for LRU.
- Compare algorithms for workloads with strong locality.
- Generate random and locality-based reference strings.
- Test 3 to 10 frames.
- Plot page faults against the number of frames.
- Measure execution time for 100,000 references.
- Verify results using hand calculations.
- Compare Clock and LRU.

## Program File
- `page_replacement.c` – Implements FIFO, LRU and Optimal algorithms and demonstrates Belady's Anomaly.

## Compilation and Execution
```bash
gcc -std=c11 -Wall -Wextra page_replacement.c -o page_replacement
./page_replacement
```

## Experimental Investigation
The program calculates page faults for 3 and 4 frames. FIFO, LRU and Optimal results are compared using the given reference string.

The Belady reference string is also tested to demonstrate the increase in FIFO page faults when the number of frames increases.

Additional experiments will use different reference strings and frame counts to generate comparison graphs and execution-time measurements.

## Conclusion
FIFO replaces the oldest loaded page, LRU replaces the least recently used page, and Optimal replaces the page whose next use is farthest in the future. LRU generally provides a practical balance between implementation complexity and page-fault performance. The final recommendation should be based on experimental results.
