---
tags:
  - Process
---
# Swap
This is one solution to the [[Producer-Consumer | producer-consumer problem]] utilizing special hardware solution. This function must be executed atomically. This cannot guarantee [[Producer-Consumer#Critical Section | bounded waiting]].
## Pseudocode
```
void swap(boolean *a, boolean *b) {
    boolean temp = *a;
    *a = *b;
    *b = temp;
}

do {
    key = TRUE;
    while(key == TRUE) {
        swap(&lock, &key); // Until lock is open, busy wait
    }
    /* Critical Section */
    lock = FALSE;
} while(TRUE);
```