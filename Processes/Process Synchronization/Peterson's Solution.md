---
tags:
  - Process
---
# Peterson's Solution
This is a proposed solution to the [[Producer-Consumer | producer-consumer problem]]. This solution works for 2 [[Process Overview | processes]] and assumes functions of `LOAD` and `STORE` are atomic (uninterruptible), but does not assume any special hardware.
## Variables
The two processes share two variables:
* `int turn`: indicates who's turn it is.
* `boolean flag[2]`: indicate if a process is ready to enter.
## Pseudocode
For processes $p_1$ and $p_2$, $p_1$'s code would look like:
```
do {
    /* Entry Section */
    flag[1] = TRUE; // p1 wishes to enter
    turn = 2;       // Set the turn to the other process
    while(flag[2] == true && turn == 2);  // Busy wait

    /* Critical Section Code */

    /* Exit Section */
    flag[1] = FALSE;
} while(TRUE);
```