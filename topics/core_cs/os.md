# Operating Systems (OS) Interview Cheatsheet 💻

## 1. Process vs. Thread
- **Process:** An executing instance of a program. Has its own private virtual address space (code, data, heap, stack). Heavy context switching overhead.
- **Thread:** Light-weight unit of CPU execution inside a process. Threads of the same process share code, data, open file descriptors, and heap, but have independent stacks and registers.

## 2. Process Scheduling Algorithms
- **First-Come, First-Served (FCFS):** Non-preemptive, suffers from convoy effect.
- **Shortest Job First (SJF) / SRTF:** Optimal average waiting time; suffers from starvation of long jobs.
- **Round Robin (RR):** Preemptive, time-quantum based; ideal for time-sharing systems.
- **Priority Scheduling:** Preemptive or non-preemptive; solved with aging to prevent starvation.

## 3. Concurrency & Synchronization
- **Critical Section:** Section of code accessing shared resources that must not be concurrently accessed by more than one thread.
- **Race Condition:** Output depends on unpredictable sequence or timing of thread execution.
- **Mutex vs. Semaphore:**
  - **Mutex:** Locking mechanism with ownership (only the thread that locked it can unlock it).
  - **Binary Semaphore:** Signaling mechanism without ownership concept.
  - **Counting Semaphore:** Controls access to a finite pool of resources (initialized to $N$).

## 4. Deadlocks
Occurs when a set of processes are blocked because each is holding a resource and waiting for another resource held by another process.
### Four Coffman Conditions (Must hold simultaneously):
1. **Mutual Exclusion:** Resources cannot be shared simultaneously.
2. **Hold and Wait:** A process is holding at least one resource and waiting for another.
3. **No Preemption:** Resources cannot be forcibly confiscated.
4. **Circular Wait:** Closed chain of processes where each waits for a resource held by the next.

### Deadlock Handling:
- Prevention (break one of the 4 conditions)
- Avoidance (Banker's Algorithm using safe state checking)
- Detection & Recovery (Wait-for graph cycle detection, process termination)
- Ignorance (Ostrich Algorithm - used by most modern OSes)

## 5. Memory Management & Virtual Memory
- **Paging:** Divides virtual memory into fixed-size pages and physical RAM into frames. Handled by Memory Management Unit (MMU) and Page Tables.
- **TLB (Translation Lookaside Buffer):** Fast hardware cache for recent virtual-to-physical address mappings.
- **Page Fault:** Interrupt raised when a program accesses a page not currently mapped in physical RAM.
- **Page Replacement Algorithms:** FIFO, LRU (Least Recently Used), Optimal (Belady's anomaly occurs in FIFO).
- **Thrashing:** System spends more time swapping pages in/out of disk than executing useful instructions.
