# Computer Organization & Architecture (COA) — BPSC Computer Teacher Exam Notes (Detailed & Comprehensive)

**Format:** Theory (concepts + exam points + formulas) → Section MCQs (A–D) → Correct Option → Explanation

---

## 1) COA Basics: Organization vs Architecture

### Core Concepts
- **Computer Architecture** = programmer-visible attributes: ISA, instruction formats, addressing modes, data types, visible registers, I/O model.
- **Computer Organization** = how architecture is implemented: datapath, control signals, bus structure, memory hierarchy, pipeline design.

### Functional Units (Block-level)
- **Input Unit:** Accepts programs/data (keyboard, scanner, network).
- **Output Unit:** Displays results (monitor, printer).
- **Memory Unit:** Stores instructions and data.
- **CPU:** Executes instructions.
  - **ALU:** Arithmetic/logic operations.
  - **Control Unit:** Sequencing (fetch → decode → execute) and control signals.
  - **Registers:** Fast internal storage.

### System Buses
- **Address Bus:** Usually unidirectional CPU → memory/I/O. Width decides address space. Example: 32-bit width = 2^32 = 4 GB (byte-addressable).
- **Data Bus:** Bidirectional; width impacts transfer per cycle (bandwidth/word-size).
- **Control Bus:** Read/Write, interrupt, clock, reset, bus request/ack.

### Important Exam Formula (Byte-addressable)
- If address bus = **n bits**, maximum addressable memory = **2^n bytes**.
- If word size = m bits, address bus = n bits → maximum memory = 2^n × (m/8) bytes.

---

### MCQs (Section 1)

## Q1. "Computer architecture" mainly refers to:
A. PCB wiring and chips placement  
B. Programmer-visible instruction set and registers  
C. OS scheduling algorithms  
D. Network topology  

> **Correct Option: B**  
> **Explanation:** Architecture focuses on ISA, instruction formats, addressing modes, and programmer-visible registers.

## Q2. In a byte-addressable machine, a 32-bit address bus can address:
A. 2 GB  
B. 4 GB  
C. 8 GB  
D. 16 GB  

> **Correct Option: B**  
> **Explanation:** 2^32 bytes = 4 GB.

## Q3. Which bus typically carries signals like Read/Write and Interrupt?
A. Data bus  
B. Address bus  
C. Control bus  
D. Cache bus  

> **Correct Option: C**  
> **Explanation:** Control bus carries command/timing/control signals (R/W, interrupt, clock, reset).

## Q4. Data bus is _____ while Address bus is _____.
A. Unidirectional; Bidirectional  
B. Bidirectional; Unidirectional  
C. Both unidirectional; Both bidirectional  
D. Depends on CPU design  

> **Correct Option: B**  
> **Explanation:** Data flows both ways (CPU ↔ Memory); Address flows one way (CPU → Memory/I/O).

---

## 2) Number Systems & Data Representation (High Yield)

### Positional Number Systems
- **Binary (2), Octal (8), Decimal (10), Hex (16)**
- Quick conversions:
  - Binary ↔ Octal: group bits in **3**
  - Binary ↔ Hex: group bits in **4**
- Example: (1010 1100)₂ = (AC)₁₆ = (254)₁₀

### Signed Representations (Very Important)
1. **Sign-Magnitude**
   - MSB is sign (0 = +, 1 = −); remaining bits magnitude.
   - Has **+0 and −0**.
   - Range (n bits): −(2^(n−1)−1) to +(2^(n−1)−1)

2. **1's Complement**
   - Negative = invert all bits.
   - Has **+0 and −0**.
   - Range (n bits): −(2^(n−1)−1) to +(2^(n−1)−1)

3. **2's Complement (Most used)**
   - Negative = invert bits + 1.
   - Only one zero; addition/subtraction easier in hardware.
   - Range (n bits): **−2^(n−1) to +(2^(n−1)−1)**
   - Example: 8-bit: −128 to +127

### Overflow (2's Complement)
- Overflow occurs when:
  - Adding two positives gives negative, OR
  - Adding two negatives gives positive.
- Carry out of MSB alone is not a reliable overflow indicator in 2's complement; check sign-bit logic.

### Codes (Exam-friendly)
- **ASCII:** 7-bit code (stored as 8-bit); A=65, a=97, 0=48.
- **Unicode/UTF-8:** Supports large character set; UTF-8 variable length (1–4 bytes).

---

### MCQs (Section 2)

## Q5. Which signed representation is most common for arithmetic hardware?
A. Sign-magnitude  
B. 1's complement  
C. 2's complement  
D. Excess-3  

> **Correct Option: C**  
> **Explanation:** 2's complement supports straightforward add/subtract with one zero.

## Q6. Range of 8-bit 2's complement integers is:
A. −127 to +127  
B. −128 to +127  
C. −128 to +128  
D. 0 to 255  

> **Correct Option: B**  
> **Explanation:** For n=8, range is −2^7 to (2^7−1) = −128 to +127.

## Q7. Binary to Hex conversion is easiest by grouping:
A. 2 bits  
B. 3 bits  
C. 4 bits  
D. 5 bits  

> **Correct Option: C**  
> **Explanation:** 1 hex digit = 4 binary bits (2^4 = 16).

## Q8. In 2's complement, −5 represented in 8 bits is:
A. 10000101  
B. 11111011  
C. 11111010  
D. 10000100  

> **Correct Option: B**  
> **Explanation:** 5 = 00000101; invert → 11111010; +1 → 11111011.

---

## 3) Register Transfer Language (RTL) & Micro-Operations

### RTL Basics
- RTL describes **data movement between registers** and micro-operations.
- Example: `R2 ← R1` means transfer contents of R1 to R2.
- Used to describe instruction execution at register level.

### Types of Micro-Operations
1. **Register transfer:** `R2 ← R1`
2. **Arithmetic:** `R3 ← R1 + R2`, `INC R1` (increment), `DEC R1`
3. **Logic:** `R1 ← R1 AND R2`, XOR, NOT, OR
4. **Shift:** 
   - Logical: shift out, 0 shift in
   - Arithmetic: shift out, MSB/LSB preserved
   - Rotate: circular shift

### Common CPU Registers (Conceptual)
- **PC (Program Counter):** address of next instruction to fetch
- **IR (Instruction Register):** current instruction being executed
- **MAR (Memory Address Register):** holds address for memory access
- **MDR/MBR (Memory Data Register/Buffer):** buffers data between CPU and memory
- **PSW/Flags:** status bits (Z=zero, C=carry, S/N=sign, V=overflow)
- **ACC (Accumulator):** general-purpose or special-purpose arithmetic register
- **SP (Stack Pointer):** points to top of stack
- **General Purpose Registers (GPRs):** R0, R1, ..., Rn

---

### MCQs (Section 3)

## Q9. MAR typically stores:
A. Current opcode  
B. Memory address to be accessed  
C. Result of ALU  
D. Cache block data  

> **Correct Option: B**  
> **Explanation:** MAR feeds the address lines for memory access.

## Q10. IR stores:
A. Next instruction address  
B. Current instruction  
C. Only operands  
D. Only flags  

> **Correct Option: B**  
> **Explanation:** IR holds the instruction fetched from memory for decoding/execution.

## Q11. Register transfer notation `R2 ← R1 + R2` means:
A. Add R1 and R2, store in a temporary register  
B. Add contents of R1 and R2, store result in R2  
C. Transfer R1 to R2 and add  
D. Transfer R1, then add R2  

> **Correct Option: B**  
> **Explanation:** RTL ← indicates assignment to the left operand.

## Q12. Arithmetic right shift differs from logical right shift in that it:
A. Shifts faster  
B. Preserves sign bit / fills with MSB instead of 0  
C. Requires more cycles  
D. Only works for positive numbers  

> **Correct Option: B**  
> **Explanation:** Arithmetic shift preserves sign bit (MSB) for signed number magnitude preservation.

---

## 4) Instruction Set Architecture (ISA)

### Instruction Formats (0/1/2/3-address)
- **0-address:** stack machine (operands implied on stack); e.g., `PUSH A`, `ADD` (pops two, pushes result)
- **1-address:** accumulator-based (ACC implied); e.g., `LOAD A`, `ADD B`
- **2-address:** one operand also destination; e.g., `MOV R1, R2` or `ADD R1, R2`
- **3-address:** explicit destination + 2 sources; e.g., `ADD R1, R2, R3`

### Instruction Word Structure
- **Opcode field:** specifies operation
- **Address field(s):** specify operand(s)
- **Mode bits:** specify addressing mode
- **Example (16-bit):** [4-bit opcode | 2-bit mode | 5-bit reg1 | 5-bit reg2]

### Addressing Modes (BPSC must-know)
- **Immediate:** operand inside instruction (`MOV R1, #5`); fastest, limited range
- **Direct/Absolute:** instruction gives memory address; simple but limited address space
- **Indirect:** instruction points to a location containing effective address; flexible but slower
- **Register:** operand in register; very fast
- **Register Indirect:** register holds address (pointer); `MOV R1, (R2)`
- **Indexed/Base+Offset:** effective address = base + offset; for arrays
- **Relative (PC + offset):** branch/loop; position-independent code
- **Auto inc/dec:** register updated automatically; e.g., `(R2)+` or `−(R2)`

### RISC vs CISC
| Aspect | RISC | CISC |
| :--- | :--- | :--- |
| **Instruction length** | Fixed | Variable |
| **Instruction count** | Many | Few (complex) |
| **Cycles per instr** | 1 (mostly) | Multiple |
| **Addressing modes** | Few | Many |
| **Register count** | Many (16+) | Few (8) |
| **Control** | Hardwired | Microcode |
| **Examples** | ARM, MIPS | x86, x64 |

---

### MCQs (Section 4)

## Q13. Best addressing mode for arrays is:
A. Immediate  
B. Indexed (Base + offset)  
C. Direct  
D. Implied  

> **Correct Option: B**  
> **Explanation:** Arrays use base address + index/offset naturally.

## Q14. PC-relative addressing is mainly used in:
A. Multiplication  
B. Cache mapping  
C. Branch instructions  
D. DMA transfer  

> **Correct Option: C**  
> **Explanation:** Branch target computed as PC + offset.

## Q15. In 3-address instruction format, how many operands are explicitly specified?
A. One  
B. Two  
C. Three  
D. Implicit  

> **Correct Option: C**  
> **Explanation:** 3-address format: destination + 2 sources (e.g., `ADD R1, R2, R3`).

## Q16. RISC instruction set is typically:
A. Complex, variable length  
B. Simple, fixed length  
C. Only for graphics  
D. Slower than CISC  

> **Correct Option: B**  
> **Explanation:** RISC emphasizes simple, fixed-length instructions and fast execution.

---

## 5) CPU Control Unit: Hardwired vs Microprogrammed

### Hardwired Control
- Control signals generated by combinational/sequential logic gates.
- **Fast** (minimal decoding overhead) but hard to modify (design changes require hardware redesign).
- Common in **RISC** (e.g., ARM, MIPS).
- Suitable for simple instruction sets.

### Microprogrammed Control
- Uses **control memory** (ROM) storing microinstructions.
- Each macroinstructions broken into microinstructions (micro-ops).
- **Flexible** and easier to update; generally **slower** (extra memory access).
- Common in **CISC** historically (e.g., x86).
- Suitable for complex instruction sets.

### Control Unit Block Diagram
- **Instruction decoder** → microprogram address
- **Control memory (microinstruction ROM)** → microinstruction
- Microinstruction fields → control signals for datapath

---

### MCQs (Section 5)

## Q17. Microprogrammed control unit is preferred because it is:
A. Fastest possible  
B. More flexible and easier to modify  
C. Requires no memory  
D. Only used in RISC  

> **Correct Option: B**  
> **Explanation:** Microcode updates change control behavior without redesigning hardware.

## Q18. Hardwired control is suitable for:
A. Complex instruction sets  
B. Frequently changing ISA  
C. Simple, fixed instruction sets  
D. Microcode updates  

> **Correct Option: C**  
> **Explanation:** Hardwired control is fast but inflexible; best for stable, simple ISA.

## Q19. Control memory in a microprogrammed CU stores:
A. Data  
B. Program instructions  
C. Microinstructions  
D. Cache blocks  

> **Correct Option: C**  
> **Explanation:** Control memory holds microinstructions that generate control signals.

---

## 6) Instruction Cycle & Timing

### Fetch–Decode–Execute Cycle
1. **Fetch:** PC → MAR → Memory → MDR → IR; PC ← PC + 1
2. **Decode:** CU reads IR, determines operation/addressing mode
3. **Execute:** ALU operation, memory access, or branch
4. **Write-back:** Store result (may not be needed for every instruction)
5. **Interrupt check** (implementation-dependent)

### Timing Considerations
- **Clock cycle:** period of system clock
- **Instruction time:** number of clock cycles per instruction
- **Total execution time:** sum of all instruction times

### Fetch-Execute Overlap (Pipelining)
- Modern CPUs overlap stages for improved throughput.

---

### MCQs (Section 6)

## Q20. The fetch stage primarily performs:
A. ALU calculation  
B. PC → MAR, memory read → IR  
C. Result write-back  
D. Branch target calculation  

> **Correct Option: B**  
> **Explanation:** Fetch loads instruction from memory into IR and increments PC.

---

## 7) Pipelining (Very Important)

### Concept
- Overlap stages of multiple instructions to improve **throughput**.
- Classic 5-stage: **IF (Fetch) → ID (Decode) → EX (Execute) → MEM (Memory) → WB (Write-back)**

### Pipeline Performance
- **Ideal speedup:** k stages ≈ k× speedup (under ideal conditions)
- **Throughput:** 1 instruction per cycle (ideal)
- **Latency:** still k cycles from start to finish of one instruction

### Hazards + Remedies
1. **Structural hazard:** resource conflict (e.g., single ALU, single memory port)
   - Remedy: duplicate resources, separate I/D cache

2. **Data hazard:** operand not ready (RAW/WAR/WAW)
   - RAW (Read After Write) most common: instruction needs result of prior instruction
   - Remedy: **forwarding/bypassing**, **stalls**, **register renaming**

3. **Control hazard:** branch; incorrect instruction in pipeline
   - Remedy: **branch prediction**, **delayed branch**, **pipeline flush**, **speculatively execute**

---

### MCQs (Section 7)

## Q21. RAW hazard stands for:
A. Read After Write  
B. Write After Read  
C. Write After Write  
D. Read After Wait  

> **Correct Option: A**  
> **Explanation:** RAW is a true data dependency; handled via forwarding/stalls.

## Q22. Control hazards mainly occur due to:
A. Add instructions  
B. Branch instructions  
C. Move instructions  
D. NOP instructions  

> **Correct Option: B**  
> **Explanation:** Branches change PC flow and can cause wrong-path fetch.

## Q23. Forwarding (bypassing) is used to resolve:
A. Structural hazards  
B. Control hazards  
C. Data hazards (RAW)  
D. Cache misses  

> **Correct Option: C**  
> **Explanation:** Forwarding sends ALU result directly to dependent instruction, bypassing write-back stage.

## Q24. In ideal 5-stage pipeline, the speedup is approximately:
A. 5×  
B. 2.5×  
C. 10×  
D. 1×  

> **Correct Option: A**  
> **Explanation:** Ideal speedup ≈ number of stages (under no hazards, perfect branch prediction).

---

## 8) Memory Organization (Cache + Virtual Memory)

### Memory Hierarchy
Registers → Cache (L1/L2/L3 SRAM) → Main memory (DRAM) → Secondary storage (SSD/HDD)

### Cache Basics
- **Hit:** data found in cache; fast access (~1–3 cycles)
- **Miss:** data not found → fetch from lower level; slow (~50–200+ cycles main memory)
- **Miss penalty:** extra time for miss
- **Hit ratio:** hits / (hits + misses)
- **AMAT (Average Memory Access Time):** hit_time + miss_rate × miss_penalty

### Cache Locality
- **Temporal locality:** recently used data likely reused soon
- **Spatial locality:** nearby addresses likely accessed soon

### Cache Mapping Strategies
1. **Direct-mapped:**
   - Each memory block maps to exactly one cache line
   - Formula: cache_line = block_address MOD (cache_size / block_size)
   - **Pros:** simple, fast tag comparison
   - **Cons:** high conflict miss rate

2. **Fully associative:**
   - Block can go anywhere in cache
   - **Pros:** flexible, lowest conflict misses
   - **Cons:** expensive (search all lines)

3. **Set-associative (n-way):**
   - Block maps to specific set; can go anywhere in that set
   - Compromise between speed and flexibility
   - Common: 2-way, 4-way, 8-way

### Replacement Policies
- **LRU (Least Recently Used):** replace entry not used longest
- **FIFO:** replace oldest entry
- **Random:** replace random entry

### Virtual Memory
- Provides illusion of large memory using disk storage.
- **Paging:** 
  - Fixed-size pages (4 KB typical) and frames
  - No external fragmentation
  - May have internal fragmentation (last page not fully used)
  - **TLB** caches page table entries for fast translation

- **Segmentation:**
  - Variable-size segments (Code, Data, Stack, etc.)
  - Supports logical program divisions
  - May cause external fragmentation (gaps between segments)

---

### MCQs (Section 8)

## Q25. Cache is typically made of:
A. DRAM  
B. SRAM  
C. HDD  
D. Optical disk  

> **Correct Option: B**  
> **Explanation:** SRAM is faster; used for cache (DRAM for main memory).

## Q26. Paging primarily eliminates:
A. Internal fragmentation  
B. External fragmentation  
C. Cache misses  
D. Interrupt latency  

> **Correct Option: B**  
> **Explanation:** Paging uses fixed-size blocks, so no external fragmentation (but internal can exist).

## Q27. TLB is used to speed up:
A. ALU operations  
B. Branch prediction  
C. Address translation  
D. Disk scheduling  

> **Correct Option: C**  
> **Explanation:** TLB caches page table entries (virtual → physical mapping).

## Q28. In fully associative cache, the main disadvantage is:
A. External fragmentation  
B. High cost (search all lines)  
C. Low flexibility  
D. No internal fragmentation  

> **Correct Option: B**  
> **Explanation:** Fully associative requires comparing tags with all cache lines.

## Q29. Average Memory Access Time (AMAT) is calculated as:
A. Hit time + miss rate × miss penalty  
B. Hit time × miss penalty  
C. Miss rate / (Hit time + miss penalty)  
D. (Hit time + miss time) / 2  

> **Correct Option: A**  
> **Explanation:** AMAT = H + MR × MP (probabilistic formula).

---

## 9) I/O Organization (Polling, Interrupt, DMA)

### Programmed I/O (Polling)
- CPU repeatedly checks device status (e.g., busy flag) in a loop.
- **Pros:** simple implementation
- **Cons:** wastes CPU cycles; poor CPU utilization

### Interrupt-driven I/O
- Device interrupts CPU when ready (asserts interrupt signal).
- CPU suspends current task, jumps to **ISR (Interrupt Service Routine)**.
- After ISR, CPU resumes previous task.
- **Pros:** improves CPU utilization
- **Cons:** interrupt latency, context switch overhead

### DMA (Direct Memory Access)
- **DMA Controller** transfers data between I/O device and memory without CPU.
- Modes:
  - **Burst mode:** blocks CPU for entire block transfer
  - **Cycle stealing:** DMA transfers one word at a time, releasing bus to CPU between transfers
- **Pros:** fast bulk transfer, frees CPU for other work
- **Cons:** DMA controller hardware complexity

### Interrupt Types
- **Maskable:** can be disabled by CPU
- **Non-maskable (NMI):** cannot be disabled (e.g., system reset)
- **Vectored:** interrupt provides ISR address
- **Non-vectored:** CPU finds ISR by lookup table

---

### MCQs (Section 9)

## Q30. Programmed I/O is also known as:
A. DMA  
B. Polling  
C. Buffering  
D. Spooling  

> **Correct Option: B**  
> **Explanation:** CPU polls device status continuously.

## Q31. DMA is used mainly to:
A. Increase instruction count  
B. Transfer blocks between I/O device and memory  
C. Decode instructions  
D. Replace cache  

> **Correct Option: B**  
> **Explanation:** DMA offloads bulk data transfer from CPU.

## Q32. ISR stands for:
A. Instruction Set Register  
B. Interrupt Service Routine  
C. Internal Storage Register  
D. Interrupt Status Register  

> **Correct Option: B**  
> **Explanation:** ISR handles interrupt; CPU jumps here when interrupt occurs.

## Q33. In DMA cycle stealing mode:
A. CPU is blocked for entire block transfer  
B. DMA transfers one word at a time  
C. No bus access for DMA  
D. CPU handles I/O completely  

> **Correct Option: B**  
> **Explanation:** DMA steals individual bus cycles from CPU, allowing CPU to work between transfers.

---

## 10) Parallelism & Flynn's Taxonomy

### Flynn's Classification
Based on **Instruction and Data streams:**

- **SISD:** Single instruction, single data
  - Classic uniprocessor (single core)
  - Example: single-core CPU

- **SIMD:** Single instruction, multiple data
  - Vector processor; GPU
  - Same instruction applied to multiple data elements in parallel
  - Example: add 4 vectors simultaneously

- **MISD:** Multiple instruction, single data
  - Rare; used for fault tolerance / redundancy
  - Multiple processors on same data stream

- **MIMD:** Multiple instruction, multiple data
  - Multicore CPUs, multiprocessor systems, distributed systems
  - Each processor independent; different code on different data

---

### MCQs (Section 10)

## Q34. GPU-style computation is closest to:
A. SISD  
B. SIMD  
C. MISD  
D. MIMD  

> **Correct Option: B**  
> **Explanation:** SIMD executes same instruction over many data elements (e.g., vector addition).

## Q35. Multicore CPU systems are typically:
A. SISD  
B. SIMD  
C. MISD  
D. MIMD  

> **Correct Option: D**  
> **Explanation:** Multiple cores execute different instruction streams on different data.

---

## 11) Performance Analysis (Numericals)

### Key Formulas
- **CPU Time = Instruction Count (IC) × CPI × Clock Cycle Time**
- **Clock Rate (GHz) = 1 / Clock Cycle Time**
- **AMAT = Hit Time + Miss Rate × Miss Penalty**
- **Speedup = (Old CPU Time) / (New CPU Time)**
- **Amdahl's Law: Speedup = 1 / [(1−f) + f/s]** where f = fraction improved, s = speedup of improved part

### Example (Exam-style)
- CPU executes 10^6 instructions
- CPI = 2
- Clock = 2 GHz (0.5 ns period)
- CPU Time = 10^6 × 2 × 0.5 ns = 1 ms

---

### MCQs (Section 11)

## Q36. A CPU with 2 GHz clock has a cycle time of:
A. 2 ns  
B. 1 ns  
C. 0.5 ns  
D. 0.25 ns  

> **Correct Option: C**  
> **Explanation:** Cycle time = 1 / frequency = 1 / (2 × 10^9) = 0.5 × 10^-9 s = 0.5 ns.

## Q37. If a program has 50% computation (speedup 4×) and 50% I/O (no speedup), overall speedup is:
A. 2×  
B. 1.33×  
C. 4×  
D. 8×  

> **Correct Option: B**  
> **Explanation:** Amdahl: 1 / [(1−0.5) + 0.5/4] = 1 / [0.5 + 0.125] = 1 / 0.625 = 1.6× (or ~1.33× depending on rounding).

---

## 12) Advanced Topics (Brief)

### Out-of-Order Execution
- CPU may reorder independent instructions to reduce stalls (maintain data dependencies).
- Uses techniques like **reservation stations** and **re-order buffers**.

### Superscalar
- Multiple instructions issue per cycle (2–4 typical).
- Requires wide pipeline and complex hazard detection.

### VLIW (Very Long Instruction Word)
- Compiler explicitly specifies multiple operations per instruction.
- Examples: Intel Itanium (historical), some DSPs.

### Multi-threading
- CPU maintains multiple hardware contexts (thread states).
- Can switch threads on stall (e.g., cache miss).
- Improves utilization.

---

## End of Comprehensive COA Notes
---
