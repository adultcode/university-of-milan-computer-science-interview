# 💻 Operating Systems — Expanded Crash Guide

> Use this as a quick review map before interviews.
> Try to explain each topic in **60–90 seconds**.

---

# 📚 Core Goal

* Understand how programs run
* Explain how the OS manages:

  * CPU
  * Memory
  * Processes
  * Threads
* Understand concurrency and memory management basics

### Most Common Interview Questions

* Program vs Process
* Process vs Thread
* Context Switching
* CPU Scheduling
* Race Conditions
* Deadlock
* Virtual Memory
* Paging
* File Systems

---

# ▶️ Program vs Process

## Program

A program is passive code stored on disk.

Examples:

* `.exe`
* Installed applications
* Source code

---

## Process

A process is a running instance of a program.

A process includes:

* Memory
* CPU state
* Stack
* Heap
* OS resources

---

## Simple Example

* Google Chrome installed on disk → Program
* Chrome currently running → Process

## ✅ Interview Answer

> A process is a running program.


---

# 🧵 Process vs Thread

## Process

* Has its own memory space
* More isolated
* More expensive to create

---

## Thread

A thread is an execution unit inside a process.

Threads:

* Share the same memory
* Are lightweight
* Run concurrently

---

## Important Trade-Off

### Advantages

* Faster communication
* Lower overhead

### Risks

* Shared memory can cause bugs

## ✅ Interview Answer

> Threads are cheaper than processes, but shared memory can cause race conditions.


---

# 🔄 Context Switching

Context switching occurs when the CPU stops executing one process/thread and starts another.

The OS:

1. Saves current state
2. Loads next state
3. Continues execution

This enables multitasking.

---

## Important Point

Too much context switching:

* Reduces performance
* Adds overhead

## ✅ Interview Answer

> Context switching is necessary for multitasking, but too much switching reduces performance.



---

# ⚙️ CPU Scheduling

CPU scheduling decides:

> Which process or thread gets CPU time next.

---

## Scheduling Goals

* Fairness
* Fast response time
* High throughput
* Priority handling

---

## Common Algorithms

| Algorithm           | Idea                        |
| ------------------- | --------------------------- |
| FCFS                | First process arrives first |
| Round Robin         | Fixed time slices           |
| Priority Scheduling | Higher priority runs first  |

---

## Round Robin

Each process gets a small time slice called a **quantum**.

If unfinished:

* It returns to the ready queue

## ✅ Interview Answer

> The scheduler chooses which ready process gets CPU time.


---

# ⚠️ Race Condition

A race condition happens when multiple threads access shared data concurrently and the result depends on timing.

---

## Example

Two threads increment a counter simultaneously:

* Final value may become incorrect

---

## Prevention Methods

* Locks
* Mutexes
* Semaphores
* Synchronization

## ✅ Interview Answer

> A race condition is a bug caused by unsafe concurrent access to shared data.



---

# 🔒 Deadlock

A deadlock occurs when processes wait forever for each other’s resources.

No process can continue.

---

# The Four Deadlock Conditions

| Condition        | Meaning                                          |
| ---------------- | ------------------------------------------------ |
| Mutual Exclusion | Resource used by one process at a time           |
| Hold and Wait    | Process holds one resource and waits for another |
| No Preemption    | Resources cannot be forcibly taken               |
| Circular Wait    | Processes wait in a cycle                        |

---

## Example

* Process A waits for resource from B
* Process B waits for resource from A

Both wait forever.

## ✅ Interview Answer

> Deadlock is a situation where no process can continue because each waits for a resource held by another.


---

# 🧠 Virtual Memory

Virtual memory gives each process the illusion of having large private memory.

The OS maps:

* Virtual addresses
  → to
* Physical memory

When RAM is insufficient:

* Disk space can be used temporarily

---

## Benefits

* Isolation between processes
* Run programs larger than RAM
* Better memory management

## ✅ Interview Answer

> Virtual memory improves isolation and allows programs to run even if physical RAM is limited.



---

# 📄 Paging

Paging divides memory into fixed-size blocks.

| Virtual Memory | Physical Memory |
| -------------- | --------------- |
| Pages          | Frames          |

---

## Page Fault

If a required page is not in RAM:

1. OS triggers page fault
2. Page loaded from disk
3. Execution continues

---

## Important Point

Disk is much slower than RAM.

Too many page faults reduce performance.

## ✅ Interview Answer

> Paging is a memory management technique that maps virtual pages to physical frames.



---

# 📁 File Systems

A file system manages:

* File storage
* File naming
* Directories
* Permissions
* Metadata
* Disk allocation

It provides an organized structure over raw storage devices.

---

## Examples

* NTFS
* FAT32
* ext4
* APFS

---

## Responsibilities

* Create/delete files
* Manage directories
* Control permissions
* Track storage blocks

## ✅ Interview Answer

> The file system provides an organized abstraction over raw storage.


---

# 🎯 Final Interview Tips

* Clearly explain process vs thread
* Mention shared memory risks with threads
* Always explain why synchronization is needed
* Use small real-world examples
* Mention performance trade-offs when discussing memory or scheduling

---

# ⚡ Quick Revision Checklist

* [ ] Program vs Process
* [ ] Process vs Thread
* [ ] Context Switching
* [ ] CPU Scheduling
* [ ] Race Conditions
* [ ] Deadlock
* [ ] Virtual Memory
* [ ] Paging
* [ ] File Systems

---

Good luck with your interview 🚀
