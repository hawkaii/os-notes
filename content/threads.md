---
threads: 
tags:
  - os
---

## Process vs Threads
- A process defines the address space text resources
- A thread defines a single sequential execution stream within a process (PC, stack , registers)
-  Threads extract the *thread of control* information from the process
- Each process may have multiple threads of control within it
  - address space of a process is shared among all its threads
  - No system calls are required to cooperate among threads
  - Simpler than message passing and shared-memory

## Kernel thread
- A kernel thread also know as a **lightweight process**, is a thread that the operating system knows about
- Switching between kernel the
## User-level threads
- OS doesn't know about the threads within the process
- own private *thread table* to keep track of the threads in  that process.
#### Advantages
- own customised scheduling algorithm
- scales better as kernel thread invariably require some table space
- Less overhead as no context switching
-  User- level thread scheduling is more flexible
  - a user-level code can define a problem dependent thread scheduling policy

- User-level threads do not require system calls to create them or context switches to move them
=> User-level threads are typically much faster than kernel threads

#### Disadvantage
- No true parallelism
  - multiple threads in process cannot run concurrently
- Since the OS does not know about the existence of the user-level threads , it may make poor scheduling decision
## Threading models
- many to one
- one to one
- many to many
- two-level



## References