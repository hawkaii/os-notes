---
tags:
  - os
---

[[define]]

*A set of processes is deadlocked if each process in the set is waiting for an event that only another process in the set can cause.*
## Detect Deadlock and Then Correct it
 - Kill all threads in the cycke

time-stamp 29 min

## Conditions for Resource Deadlocks

1. **Mutual exclusion condition**. Each resource is either currently assigned to exactly one process or is available.
2. **Hold and wait condition**. Processes currently holding resources that were granted earlier can request new resources
3. **No-preemption condition**. Resources previously granted cannot be forcibly taken away form a process. They must be explicitly released by the process holding them.
4. **Circular wait condition**. There must be a circular list of two or more processes each of which is waiting for a resource held by the next remember of the chain

## Deadlock prevention
1. Mutual Exclusion: make resource sharable (but  not all resource s can be shared)
2. Hold and wait
   - guarantee that a thread cannot hold one  resource when it requests another
   - make thread request all the resources the need at one and make thread realease all resource before requesting a new set
1. No preemption
2. circular wait: impose ordering

## Deadlock Avoidance  !!

- This approach allows the three necessary conditions of deadlock but makes judicious choices to assure that deadlock point is never reached 
-  Deadlock avoidance allows more concurrency than prevention
-  A decision is made dynamically whether the current resource allocation request will, if granted potentially lead to a deadlock
-  it requires the knowledge of future process requests
- Two techniques to avoid deadlock 
  - Process Inition  Denial
  - Resource Allocation Denial
---
- Threads provide advance information about the maximum resources they may need during execution
- define a 
## references