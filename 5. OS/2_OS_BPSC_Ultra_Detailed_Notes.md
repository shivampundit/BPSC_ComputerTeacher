# Operating System (OS) — BPSC Computer Teacher Notes (Ultra Detailed)

**Format:** Detailed Theory + Comparative Tables + Formulas + Unix Commands → Topic-wise MCQs (A–D) → Correct Option → Explanation

---

## 1. Introduction & Structure

### What is an Operating System?
- **Resource Manager:** Manages CPU (Process), RAM (Memory), Disk (Storage), I/O.
- **Extended Machine:** Provides a simple interface (system calls) over complex hardware.

### Types of Operating Systems
| Type | Characteristics | Examples |
|---|---|---|
| **Batch** | Jobs grouped in batches; No interaction | IBM OS/360 |
| **Multiprogramming** | Multiple jobs in memory; CPU switches on I/O wait | Early Unix, Windows |
| **Time-Sharing (Multitasking)** | Frequent switching (quantum); Illusion of parallelism | Linux, Windows 10/11 |
| **Real-Time (RTOS)** | Strict deadlines (Hard vs Soft) | VxWorks, QNX, Medical Systems |
| **Distributed** | Tightly/Loosely coupled systems | Solaris MC, LOCUS |

### Kernel Architectures
| Architecture | Description | Pros | Cons | Examples |
|---|---|---|---|---|
| **Monolithic** | Entire OS in kernel space | High Performance | Crash affects all | Linux, Unix, MS-DOS |
| **Microkernel** | Minimal kernel; services in user space | Stability, Security | Performance overhead | Minix, QNX |
| **Hybrid** | Mix of both | Balance | Complexity | Windows NT, macOS |

### System Calls
- Interface between User Mode and Kernel Mode.
- Types: Process Control (`fork`, `exec`), File Mgmt (`open`, `read`), Device Mgmt, Info Maint, Communication.

---

### MCQs (Section 1)

## Q1. In a Time-Sharing OS, the time slice is called:
A. Latency
B. Quantum
C. Response time
D. Seek time

> **Correct Option: B**
> **Explanation:** A time quantum is the small unit of time assigned to each process in Round Robin.

## Q2. Which system call is used to create a new process in Unix?
A. create()
B. new()
C. fork()
D. spawn()

> **Correct Option: C**
> **Explanation:** `fork()` creates a child process identical to the parent.

---

## 2. Process Management

### Process State Models
- **5-State Model:** New → Ready → Running → Waiting/Blocked → Terminated.
- **7-State Model:** Adds "Suspended Ready" and "Suspended Wait" (swapped out to disk).

### Process Control Block (PCB)
- **PID:** Process ID
- **Program Counter:** Next instruction address
- **CPU Registers:** Context data
- **Scheduling Info:** Priority, pointers
- **Memory Info:** Base/Limit registers, Page tables

### CPU Scheduling Algorithms
| Algorithm | Type | Description | Pros | Cons |
|---|---|---|---|---|
| **FCFS** | Non-preemptive | Queue order | Simple | Convoy Effect |
| **SJF** | Non-preemptive | Shortest burst first | Min Avg Waiting Time | Starvation |
| **SRTF** | Preemptive | Shortest remaining time | Optimal Waiting Time | Context switch overhead |
| **Round Robin** | Preemptive | Time Quantum (TQ) | Fair, Responsive | Perf depends on TQ |
| **Priority** | Both | Highest priority first | Importance based | Starvation (Aging solves it) |

### Scheduling Metrics (Formulas)
- **Turnaround Time (TAT)** = Completion Time (CT) − Arrival Time (AT)
- **Waiting Time (WT)** = TAT − Burst Time (BT)
- **Response Time** = Time first scheduled − Arrival Time

---

### MCQs (Section 2)

## Q3. Which scheduling algorithm results in the minimum average waiting time?
A. FCFS
B. SJF (Non-preemptive)
C. Round Robin
D. SRTF (Preemptive SJF)

> **Correct Option: D**
> **Explanation:** SRTF is theoretically optimal for minimizing average waiting time.

## Q4. The solution to starvation in Priority Scheduling is:
A. Context Switching
B. Aging
C. Swapping
D. Killing process

> **Correct Option: B**
> **Explanation:** Aging gradually increases the priority of waiting processes.

---

## 3. Threads & Concurrency

### Process vs Thread
| Feature | Process | Thread |
|---|---|---|
| **Definition** | Heavyweight execution unit | Lightweight execution unit |
| **Memory** | Independent address space | Shares address space (Code/Data/Heap) |
| **Creation** | Slow (OS resource allocation) | Fast |
| **Context Switch** | Heavy overhead | Low overhead |

### Multithreading Models
- **Many-to-One:** Many user threads → 1 kernel thread. (Blocks if one blocks)
- **One-to-One:** 1 user thread → 1 kernel thread. (True concurrency)
- **Many-to-Many:** M user threads → N kernel threads.

---

### MCQs (Section 3)

## Q5. Threads belonging to the same process share:
A. Stack
B. Data section & Code section
C. Registers
D. Program Counter

> **Correct Option: B**
> **Explanation:** Threads share global variables (Data) and instructions (Code) but have private Stack/Registers.

---

## 4. Process Synchronization

### The Problem
- **Race Condition:** Outcome depends on execution order.
- **Critical Section (CS):** Shared resource access code.

### Criteria for Solution
1. **Mutual Exclusion:** Max 1 process in CS.
2. **Progress:** No deadlock in entering CS.
3. **Bounded Waiting:** No starvation.

### Tools
- **Semaphores:** Integer variable S.
  - `wait(S)` / `P(S)`: Decrement; block if < 0.
  - `signal(S)` / `V(S)`: Increment; wake up.
- **Binary Semaphore (Mutex):** 0 or 1.
- **Counting Semaphore:** Manage N instances of a resource.
- **Monitors:** High-level construct (Java `synchronized`).

### Classic Problems
- Producer-Consumer (Bounded Buffer)
- Readers-Writers Problem
- Dining Philosophers Problem

---

### MCQs (Section 4)

## Q6. A semaphore is strictly an integer variable modified by:
A. Only 'wait' operation
B. Only 'signal' operation
C. Atomic 'wait' and 'signal' operations
D. Ordinary arithmetic operations

> **Correct Option: C**
> **Explanation:** Semaphore operations must be atomic (indivisible) to ensure correctness.

---

## 5. Deadlocks

### Necessary Conditions (Coffman Conditions)
Deadlock occurs if **ALL 4** happen:
1. **Mutual Exclusion**
2. **Hold and Wait**
3. **No Preemption**
4. **Circular Wait**

### Handling Strategies
| Strategy | Method | Example |
|---|---|---|
| **Prevention** | Invalidate one condition | Spooling (No Mutex), Request all at start (No Hold & Wait) |
| **Avoidance** | Dynamic check | Banker’s Algorithm (Safe Sequence) |
| **Detection** | Check Resource Allocation Graph (RAG) | Periodically run detection algo |
| **Recovery** | Break deadlock | Kill process, Preempt resource |
| **Ignorance** | Do nothing | Ostrich Algorithm (Unix/Windows default) |

---

### MCQs (Section 5)

## Q7. Banker’s algorithm is used for:
A. Deadlock Prevention
B. Deadlock Avoidance
C. Deadlock Detection
D. Deadlock Recovery

> **Correct Option: B**
> **Explanation:** It simulates allocation to see if the system stays in a "Safe State".

---

## 6. Memory Management

### Basics
- **MMU:** Hardware mapping Logical (Virtual) → Physical Address.
- **Logical Address Space:** Defined by CPU capability (e.g., 32-bit = 4GB).
- **Physical Address Space:** Actual RAM size.

### Techniques
1. **Contiguous Allocation:** Fixed vs Variable partitions.
   - **External Fragmentation:** Free space exists but not contiguous.
   - **Internal Fragmentation:** Allocated block > requested size.
2. **Paging:** Non-contiguous.
   - **Frames:** Physical memory blocks (fixed size).
   - **Pages:** Logical memory blocks (same size).
   - **Page Table:** Maps Page# → Frame#.
   - **TLB:** Hardware cache for Page Table (speeds up access).
3. **Segmentation:** Logical units (Main, Stack, Symbol Table).

### Comparison
| Feature | Paging | Segmentation |
|---|---|---|
| **View** | Physical (System) view | Logical (User) view |
| **Fragmentation** | Internal (last page) | External |
| **Size** | Fixed size | Variable size |

---

### MCQs (Section 6)

## Q8. The mapping of logical to physical address is done by:
A. CPU
B. Compiler
C. MMU (Memory Management Unit)
D. Loader

> **Correct Option: C**
> **Explanation:** MMU is the hardware device performing runtime address translation.

## Q9. Which technique suffers from Internal Fragmentation?
A. Segmentation
B. Paging
C. Variable Partitioning
D. Demand Paging

> **Correct Option: B**
> **Explanation:** If a process needs 10.1 KB and page size is 4KB, it gets 3 pages (12KB), wasting 1.9 KB inside the last page.

---

## 7. Virtual Memory

### Concepts
- **Demand Paging:** Load pages only on Page Fault.
- **Page Fault:** Accessing a page not in RAM → OS Trap → I/O.
- **Thrashing:** High paging activity; CPU utilization drops near zero.
- **Locality of Reference:** Spatial (nearby) & Temporal (recent) access patterns prevent thrashing.

### Page Replacement Algorithms
| Algorithm | Description | Note |
|---|---|---|
| **FIFO** | Oldest page out | Belady’s Anomaly (More frames = More faults) |
| **Optimal** | Furthest in future out | Best possible (theoretical) |
| **LRU** | Least Recently Used out | Good approximation; uses Stack/Counter |
| **Clock (Second Chance)** | FIFO with reference bit | Efficient hardware support |

### Effective Access Time (EAT)
- EAT = (1−p) × MemoryTime + p × PageFaultTime
- (p is page fault rate)

---

### MCQs (Section 7)

## Q10. Belady’s Anomaly is characteristic of:
A. LRU
B. FIFO
C. Optimal
D. Stack algorithm

> **Correct Option: B**
> **Explanation:** In FIFO, increasing memory frames can paradoxically increase page faults.

---

## 8. Disk Management

### Disk Structure
- Platter → Surface → Track → Sector.
- **Seek Time:** Move arm to track (Major cost).
- **Rotational Latency:** Wait for sector.
- **Transfer Time:** Read data.

### Scheduling Algorithms
| Algo | Logic | Pros/Cons |
|---|---|---|
| **FCFS** | Order of arrival | Fair but slow |
| **SSTF** | Shortest seek first | Fast; Starvation possible |
| **SCAN** | Elevator (End-to-end) | Good uniform performance |
| **C-SCAN** | Circular Elevator | More uniform wait time |
| **LOOK** | SCAN without end | Optimization |

---

### MCQs (Section 8)

## Q11. Which disk scheduling algorithm is known as the Elevator algorithm?
A. SSTF
B. FCFS
C. SCAN
D. C-SCAN

> **Correct Option: C**
> **Explanation:** The disk arm moves back and forth like an elevator.

---

## 9. File System Implementation

### Directory Structure
- **Single-level:** All files in one dir (Naming collision).
- **Two-level:** User specific dirs.
- **Tree-structured:** Standard hierarchy.
- **Acyclic Graph:** Allows sharing (links/aliases).

### Allocation Methods
| Method | Description | Random Access? | Fragmentation? |
|---|---|---|---|
| **Contiguous** | Continuous blocks | Yes (Fastest) | External |
| **Linked** | Linked list of blocks | No (Slow) | No external |
| **Indexed** | Index block pointers | Yes | Overhead of index block |

### Unix Inode
- Contains metadata (permissions, owner, timestamps).
- Pointers: Direct (12), Single Indirect, Double Indirect, Triple Indirect.

---

### MCQs (Section 9)

## Q12. In Unix, file metadata is stored in:
A. Superblock
B. Inode
C. Boot block
D. Data block

> **Correct Option: B**
> **Explanation:** Inode (Index Node) holds attributes and disk block pointers.

---

## 10. Unix/Linux Commands (BPSC Syllabus)

### Essential Commands
| Command | Function |
|---|---|
| `ls` | List files (`-l` long, `-a` all) |
| `cp`, `mv`, `rm` | Copy, Move, Remove |
| `chmod` | Change permissions (`chmod 777 file`) |
| `chown` | Change owner |
| `grep` | Search pattern in file |
| `ps` | Process status |
| `kill` | Terminate process (`kill -9 PID`) |
| `top` | Real-time system monitor |
| `cat` | Display file content |
| `touch` | Create empty file / update timestamp |

### Permissions (rwx)
- **r (4), w (2), x (1)**
- Owner / Group / Others
- Example: `755` = `rwx` (Owner), `r-x` (Group), `r-x` (Others).

---

### MCQs (Section 10)

## Q13. Which command changes file permissions?
A. chown
B. chgrp
C. chmod
D. pwd

> **Correct Option: C**
> **Explanation:** `chmod` (change mode) modifies access permissions.

## Q14. What does `chmod 777` imply?
A. Read only for everyone
B. Read/Write/Execute for Owner, Group, and Others
C. No permissions
D. Execute only

> **Correct Option: B**
> **Explanation:** 7 = 4+2+1 (rwx). 777 means full permissions for all.

---

## End of Ultra Detailed OS Notes
