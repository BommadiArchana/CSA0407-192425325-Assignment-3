# Q1 – Linking, Loading and Address Binding

## Objective
To study and compare static linking and dynamic linking in a banking application and understand how libraries are loaded and mapped into memory.

## Requirements Covered
- Implement static and dynamic linking.
- Compare executable file sizes.
- Identify shared libraries using Linux commands.
- Demonstrate runtime library loading using `dlopen()` and `dlsym()`.
- Display program and library memory addresses using `/proc/self/maps`.
- Explain compile-time, load-time and execution-time address binding.
- Explain the roles of the linker and loader.
- Evaluate position-independent code.
- Measure startup time and memory usage.
- Test library replacement, shared pages and missing-library conditions.

## Program Files
- `bank_linking.c` – Banking application and encryption demonstration.
- Additional library-loading programs will be included for the runtime loading experiments.

## Compilation and Execution
```bash
gcc -static bank_linking.c -o bank_static
./bank_static

gcc bank_linking.c -o bank_dynamic
./bank_dynamic
```

## Experimental Investigation
The static and dynamic executable sizes are compared using `ls -lh`. Shared library dependencies are checked using `ldd`. Startup time and memory usage are measured using `/usr/bin/time -v`.

Library replacement and missing-library behaviour are tested using compatible shared libraries.

## Conclusion
Static linking includes library code in the executable, whereas dynamic linking uses separate shared libraries. Dynamic linking is generally suitable for the banking application because compatible shared libraries can be updated without rebuilding every executable. Runtime loading provides additional flexibility when a library is needed only during execution.
