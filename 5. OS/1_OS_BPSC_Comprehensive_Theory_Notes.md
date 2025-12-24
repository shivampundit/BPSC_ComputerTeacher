# Operating System (OS) — BPSC Computer Teacher Notes (Detailed & Comprehensive)

**Format:** Detailed Theory + Comparison Tables + Exam Formulas → Section MCQs (A–D) → Correct Option → Explanation

---

## 1. Introduction & Types of OS

### What is an OS?
- An **interface** between user/applications and hardware.
- **Resource Manager:** manages CPU, memory, I/O devices, files.

### Types of Operating Systems
| Type | Key Feature | Example |
|---|---|---|
| **Batch OS** | Jobs processed in batches; no user interaction | IBM OS/360 |
| **Multiprogramming** | Multiple jobs in memory; CPU switches on I/O wait | Windows, Linux |
| **Multitasking (Time-Sharing)** | CPU switches rapidly (time slice); illusion of concurrency | Unix, Windows |
| **Real-Time (RTOS)** | Strict timing constraints (Hard vs Soft) | VxWorks, QNX |
| **Distributed OS** | Multiple independent nodes appear as one | Solaris MC |

### Kernel Types
- **Monolithic Kernel:** OS services in kernel space (fast, less stable). Example: Linux, Unix.
- **Microkernel:** Minimal kernel; services in user space (stable, slower). Example: Minix, QNX.

---

### MCQs (Section 1)

## Q1. Which OS type guarantees response within strict time constraints?
A. Batch Processing
B. Real-Time OS (RTOS)
C. Distributed OS
D. Multiprogramming

> **Correct Option: B**
> **Explanation:** RTOS (like in medical/flight systems) must meet deadlines.

## Q2. In a monolithic kernel, OS services run in:
A. User space
B. Kernel space
C. Separate processes
D. Virtual machine

> **Correct Option: B**
> **Explanation:** Entire OS runs in kernel mode for performance.

---

## 2. Process Management

### Process State Diagram (5-State Model)
1. **New:** Process being created.
2. **Ready:** Waiting for CPU.
3. **Running:** Executing on CPU.
4. **Waiting/Blocked:** Waiting for I/O or event.
5. **Terminated:** Execution finished.

### Process Control Block (PCB)
- Data structure storing process info: Process ID (PID), PC, Registers, State, Priority.

### Scheduling Times
- **Arrival Time (AT):** Time process enters ready queue.
- **Burst Time (BT):** Time required for CPU execution.
- **Completion Time (CT):** Time process finishes.
- **Turnaround Time (TAT):** CT − AT.
- **Waiting Time (WT):** TAT − BT.

### Scheduling Algorithms
| Algorithm | Type | Description | Pros/Cons |
|---|---|---|---|
| **FCFS** | Non-preemptive | First Come First Serve | Convoy effect (long wait) |
| **SJF** | Non-preemptive | Shortest Job First | Optimal average WT; Starvation possible |
| **SRTF** | Preemptive | Shortest Remaining Time First | Optimal WT; Overhead |
| **Round Robin** | Preemptive | Time Quantum (TQ) based | Fair; Context switch overhead |
| **Priority** | Both | Based on priority number | Starvation possible (aging solves it) |

---

### MCQs (Section 2)

## Q3. Which scheduler selects a process from the ready queue to execute?
A. Long-term scheduler
B. Short-term scheduler
C. Medium-term scheduler
D. I/O scheduler

> **Correct Option: B**
> **Explanation:** Short-term scheduler (CPU scheduler) picks from Ready to Running.

## Q4. The "Convoy Effect" is associated with:
A. Round Robin
B. SJF
C. FCFS
D. Priority Scheduling

> **Correct Option: C**
> **Explanation:** Short processes wait behind a long process in FCFS.

---

## 3. Process Synchronization

### The Problem
- **Race Condition:** Output depends on execution order of concurrent processes.
- **Critical Section (CS):** Code accessing shared resources.

### Requirements for Solution
1. **Mutual Exclusion:** Only one process in CS at a time.
2. **Progress:** If CS is empty, selection shouldn't be postponed indefinitely.
3. **Bounded Waiting:** Limit on waiting times.

### Synchronization Tools
- **Semaphores:** Integer variable accessed via `wait()` (P) and `signal()` (V).
  - **Binary Semaphore:** Values 0, 1 (Mutex).
  - **Counting Semaphore:** Values 0 to N (Resource counting).
- **Mutex Locks:** acquire() / release().

---

### MCQs (Section 3)

## Q5. A binary semaphore takes values:
A. 0 and 1
B. 0 to N
C. -1 to 1
D. Any integer

> **Correct Option: A**
> **Explanation:** Binary semaphore acts like a lock (0 or 1).

## Q6. "Mutual Exclusion" means:
A. Multiple processes in CS
B. Only one process in CS at a time
C. No process in CS
D. Deadlock occurrence

> **Correct Option: B**
> **Explanation:** Only one process can execute in the Critical Section at once.

---

## 4. Deadlocks

### Necessary Conditions (Coffman Conditions)
Deadlock arises if **ALL 4** hold simultaneously:
1. **Mutual Exclusion:** Non-sharable resources.
2. **Hold and Wait:** Holding one resource, waiting for another.
3. **No Preemption:** Resources cannot be forcibly taken.
4. **Circular Wait:** Chain of waiting processes P1→P2→...→Pn→P1.

### Handling Deadlocks
1. **Prevention:** Disallow one of the 4 conditions.
2. **Avoidance:** Banker's Algorithm (check Safe State).
3. **Detection & Recovery:** Detect cycle, kill process.
4. **Ignorance:** Ostrich Algorithm (ignore it, typical in Unix/Windows).

---

### MCQs (Section 4)

## Q7. Banker's Algorithm is used for:
A. Deadlock Prevention
B. Deadlock Avoidance
C. Deadlock Detection
D. Deadlock Recovery

> **Correct Option: B**
> **Explanation:** It simulates allocation to check if a safe sequence exists.

## Q8. Which condition is required for a deadlock?
A. Mutual Exclusion
B. Hold and Wait
C. Circular Wait
D. All of the above

> **Correct Option: D**
> **Explanation:** All four Coffman conditions must hold simultaneously.

---

## 5. Memory Management

### Basics
- **Logical Address:** Generated by CPU (Virtual).
- **Physical Address:** Actual location in RAM.
- **MMU (Memory Management Unit):** Maps Logical → Physical.

### Contiguous Allocation
- **Fixed Partitioning:** Fixed size blocks (Internal Fragmentation).
- **Variable Partitioning:** Variable size (External Fragmentation).
- **Compaction:** Solves external fragmentation by shuffling.

### Paging (Non-contiguous)
- Process divided into **Pages**.
- Memory divided into **Frames**.
- **Page Table:** Maps Page# → Frame#.
- **TLB (Translation Lookaside Buffer):** Cache for page table entries.
- **Fragmentation:** No external; small internal (last page).

### Segmentation
- Logical divisions (Code, Stack, Data).
- suffers from External Fragmentation.

---

### MCQs (Section 5)

## Q9. Paging suffers from:
A. External Fragmentation
B. Internal Fragmentation
C. Both
D. None

> **Correct Option: B**
> **Explanation:** Paging eliminates external fragmentation but the last page may have unused space (internal).

## Q10. TLB is used to:
A. Store files
B. Speed up address translation
C. Handle interrupts
D. Manage deadlock

> **Correct Option: B**
> **Explanation:** TLB caches recent page table translations to reduce memory access time.

---

## 6. Virtual Memory

### Concept
- Process size can exceed physical memory.
- Uses **Demand Paging** (load page only when needed).

### Page Fault
- Accessed page not in memory → Trap to OS → I/O to fetch from disk.

### Page Replacement Algorithms
| Algorithm | Strategy | Pros/Cons |
|---|---|---|
| **FIFO** | Replace oldest page | Belady's Anomaly (more frames = more faults) |
| **Optimal (OPT)** | Replace page needed furthest in future | Impossible to implement (needs future knowledge) |
| **LRU** | Replace least recently used | Good approximation of OPT |

### Thrashing
- High page fault rate → CPU utilization drops (CPU busy swapping).

---

### MCQs (Section 6)

## Q11. "Belady's Anomaly" is seen in:
A. LRU
B. FIFO
C. Optimal
D. LFU

> **Correct Option: B**
> **Explanation:** In FIFO, increasing frame count can sometimes increase page faults.

## Q12. Thrashing occurs when:
A. CPU utilization is high
B. Page fault rate is very high
C. No page faults
D. Deadlock occurs

> **Correct Option: B**
> **Explanation:** System spends most time swapping pages rather than executing.

---

## 7. Disk Scheduling

### Goal
- Minimize **Seek Time** (head movement).

### Algorithms
| Algo | Description | Note |
|---|---|---|
| **FCFS** | In order of requests | High seek time |
| **SSTF** | Shortest Seek Time First | Minimize immediate movement; Starvation possible |
| **SCAN** | Elevator (move to end, reverse) | Good for uniform load |
| **C-SCAN** | Circular SCAN (wrap around) | More uniform wait time |
| **LOOK/C-LOOK** | SCAN without going to physical end | Optimization of SCAN |

---

### MCQs (Section 7)

## Q13. Which disk scheduling algorithm acts like an elevator?
A. FCFS
B. SSTF
C. SCAN
D. C-LOOK

> **Correct Option: C**
> **Explanation:** SCAN moves to one end servicing requests, then reverses.

---

## 8. File Systems

### Access Methods
- **Sequential:** Read byte by byte (Tape).
- **Direct/Random:** Jump to block (Disk).

### Allocation Methods
| Method | Description | Pros/Cons |
|---|---|---|
| **Contiguous** | Continuous blocks | Fast; External fragmentation |
| **Linked** | Linked list of blocks | No ext frag; Slow random access |
| **Indexed** | Index block holds pointers | Supports random access; Pointer overhead |

### Unix Inode
- Uses indexed allocation (Direct + Single/Double/Triple Indirect pointers).

---

### MCQs (Section 8)

## Q14. Which allocation method supports direct access best without fragmentation?
A. Contiguous
B. Linked
C. Indexed
D. Stack

> **Correct Option: C**
> **Explanation:** Indexed allocation keeps pointers in an index block, allowing direct access.

---
