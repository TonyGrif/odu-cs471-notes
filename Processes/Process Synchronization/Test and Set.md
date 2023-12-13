---
tags:
  - Process
---
# Test and Set
This is one solution to the [[Producer-Consumer | producer-consumer problem]] utilizing special hardware solution. This function is run atomically. This method cannot guarantee [[Producer-Consumer#Critical Section | bounded waiting]].
## Pseudocode
```
boolean test_and_set(boolean *target) {
    boolean return_value = *target;
    *target = TRUE;
    return return_value;
}

do {
    while(test_and_set(&lock)); // Busy waiting until lock open
    /* Critical Section */
    lock = FALSE;
} while(TRUE);
```