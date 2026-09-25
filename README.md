# Project Overview
This repository contains a single C source file (`sort.c`) that implements an optimized version of the classic **Bubble Sort** algorithm. The implementation includes helper functions for swapping elements and printing an array, and demonstrates sorting a hard‑coded integer array in `main`.

# Tech Stack
- **Language**: C (C99 compatible)
- **Build Tool**: GCC or any ISO‑C compiler that supports C99

# Features
- **Optimized Bubble Sort**: The inner loop can terminate early if no swaps occur during a pass, reducing unnecessary comparisons.
- **Utility Functions**:  
  - `swap(int*, int*)` – Swaps two integer values.  
  - `printArray(int[], int)` – Prints the contents of an array.
- **Demonstration**: `main` shows the algorithm in action on a sample dataset.

# Project Structure
```
sort.c            # Single source file containing the entire program
```

# Local Setup
1. **Compile**  
   ```bash
   gcc -std=c99 -Wall -Wextra -o sort sort.c
   ```
2. **Run**  
   ```bash
   ./sort
   ```

# Usage Flow
After compiling, executing the binary prints the sorted array:

```
Sorted array: 
11 12 22 25 34 64 90 
```

# Safety Notes
- The code uses `<stdbool.h>` for the `bool` type; ensure your compiler supports C99 or later.  
- **Bug Notice**: The inner loop in `bubbleSort` is incomplete (`for (j = 0; j < )`). This will cause a compilation error. A typical fix is:
  ```c
  for (j = 0; j < n - i - 1; j++)
  ```
  or adjust the logic to iterate over the unsorted portion of the array.

# Roadmap
- **Add more sorting algorithms** (e.g., quick sort, merge sort) for comparison.  
- **Unit Testing**: Integrate a C testing framework like Unity to automate validation.  
- **Modularization**: Separate helper functions into header/source files for clarity and reusability.

---
