# Contiguous-Binary

The provided assembly code consists of two parts, each with its own purpose and functionality.

# Part 2:
This part of the code is designed to find the length of the longest contiguous string of 1s in a binary number.

The _start section initializes registers and sets up the loop.
It enters a loop (LOOP) where it decrements R3 (counter) until it reaches zero.
Inside the loop, it calls a subroutine ONES which counts the length of the consecutive 1s in the binary number stored in memory.
After counting, it loads the next word from memory (TEST_NUM) into R1.
It compares the result of ONES with the current maximum length stored in R5 and updates R5 if necessary.
Finally, it continues the loop until R3 reaches zero.

# Part 3:
This part extends the functionality of the previous part by adding the ability to find the longest contiguous string of 0s and performing alternating digit checks.

_start initializes registers and sets up the loop similar to Part 2.
Inside the loop, it calls three subroutines: ONES, ZEROES, and ALTERNATE.
ONES and ZEROES are similar to Part 2 but ZEROES operates on inverted data.
ALTERNATE first loads a data template ALT_DATA, performs an XOR operation with the current data, calls ONES and ZEROES on the result, then compares the lengths of the strings of 1s and 0s to determine the longest string. The result is stored in R0.
After each subroutine call, it compares the result with the current maximum and updates the maximum if necessary.
The loop continues until R3 reaches zero.
Overall Functionality:
Part 2: Finds the length of the longest string of 1s in a binary number.
Part 3: Extends the functionality to find the length of the longest string of 0s and perform alternating digit checks, updating the maximum lengths accordingly.
The code appears to be written in ARM assembly language, targeting a specific architecture or processor. It operates on binary data stored in memory (TEST_NUM) and uses various bitwise operations to manipulate and analyze the data.
