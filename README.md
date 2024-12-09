# COBOL Data Type Overflow Bug

This repository demonstrates a subtle data type overflow bug that can occur in COBOL programs. The program calculates the sum of numbers from 1 to 10. While seemingly straightforward, it contains a potential error related to data type handling if the data type is not large enough to hold the result.

## Bug Description

The `WS-TOTAL` variable might be declared with a data type that is too small to hold the sum of numbers from 1 to 10 (which is 55).  If this is the case, an overflow can occur leading to an incorrect result.

## Solution

The solution involves using a data type for `WS-TOTAL` that is large enough to store the result without overflow.

## How to Reproduce

1. Compile the `bug.cob` file.
2. Run the compiled program.
3. Observe the output.  If the output is not 55, an overflow has occurred.

## How to Fix

1. Modify the `bug.cob` file to use a larger data type for `WS-TOTAL`. See `bugSolution.cob` for the corrected code.
2. Recompile and run the fixed program to verify the result is 55.