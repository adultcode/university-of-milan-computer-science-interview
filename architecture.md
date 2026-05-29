# 🖥️ Computer Architecture — Expanded Crash Guide

> Use this as a quick review map before interviews.
> Try to explain each topic in **60–90 seconds**.

---

# 📚 Core Goal

* Understand how CPUs execute instructions
* Learn memory hierarchy concepts
* Understand performance optimization techniques
* Learn basic digital logic concepts

### Most Common Interview Questions

* CPU Instruction Cycle
* Registers
* Cache Memory
* Memory Hierarchy
* RAM vs ROM
* Pipelining
* Pipeline Flush
* Logic Gates

---

# ⚙️ CPU & Instruction Cycle

The CPU executes instructions repeatedly through several stages.

---

# Common Instruction Cycle Stages

| Stage         | Purpose                     |
| ------------- | --------------------------- |
| Fetch         | Get instruction from memory |
| Decode        | Understand instruction      |
| Execute       | Perform operation           |
| Memory Access | Read/write memory if needed |
| Write Back    | Store result                |

---

## Example

For:

```text id="cpu-example"
a = b + c
```

The CPU:

1. Fetches instruction
2. Decodes addition operation
3. Loads values
4. Executes addition
5. Stores result

---

## Important Point

The exact stages depend on CPU architecture.

## ✅ Interview Answer

> The CPU repeatedly fetches instructions, decodes them, and executes them.


---

# 🧠 Registers

Registers are tiny, ultra-fast storage locations inside the CPU.

They store:

* Temporary values
* Addresses
* Control information

---

## Important Characteristics

| Property | Description    |
| -------- | -------------- |
| Speed    | Fastest memory |
| Size     | Very small     |
| Location | Inside CPU     |

---

## Examples

* Program Counter (PC)
* Instruction Register (IR)
* Stack Pointer (SP)

## ✅ Interview Answer

> Registers are the fastest storage in the memory hierarchy.


---

# ⚡ Cache Memory

Cache is small, fast memory located between CPU and RAM.

It stores:

* Frequently used data
* Recently accessed instructions

Goal:

> Reduce average memory access time.

---

# Cache Levels

| Cache | Speed   | Size     |
| ----- | ------- | -------- |
| L1    | Fastest | Smallest |
| L2    | Medium  | Larger   |
| L3    | Slower  | Largest  |

---

## Why Cache Matters

RAM is much slower than CPU speed.

Without cache:

* CPU would wait frequently for memory access

## ✅ Interview Answer

> Cache improves performance because accessing RAM is much slower than accessing CPU cache.


---

# 🏗️ Memory Hierarchy

Memory hierarchy organizes storage based on:

* Speed
* Size
* Cost

---

# Typical Hierarchy

```text id="memory-hierarchy"
Registers
↓
Cache
↓
RAM
↓
SSD / HDD
↓
Cloud / External Storage
```

---

## Important Rule

* Faster memory → smaller & more expensive
* Slower memory → larger & cheaper

## ✅ Interview Answer

> The hierarchy balances speed and capacity.



---

# 💾 RAM (Random Access Memory)

RAM is the main memory used for active programs and data.

---

## Characteristics

| Property | Description              |
| -------- | ------------------------ |
| Volatile | Loses data without power |
| Speed    | Faster than storage      |
| Usage    | Running programs         |

---

## Example

When opening:

* Browser
* IDE
* Game

Data is loaded into RAM.

## ✅ Interview Answer

> RAM is temporary working memory for active programs.



---

# 📀 ROM (Read-Only Memory)

ROM is non-volatile memory.

It stores:

* Firmware
* Boot instructions
* BIOS/UEFI code

Data remains even without power.

---

## Example

When computer starts:

* ROM provides startup instructions

## ✅ Interview Answer

> ROM is used for firmware and boot instructions.



---

# 🚀 Pipelining

Pipelining improves CPU throughput by overlapping instruction stages.

---

## Idea

Instead of finishing one instruction completely before starting another:

Multiple instructions run simultaneously in different stages.

---

## Example

| Instruction   | Stage   |
| ------------- | ------- |
| Instruction 1 | Execute |
| Instruction 2 | Decode  |
| Instruction 3 | Fetch   |

---

## Important Point

Pipelining:

* Increases throughput
* Does NOT necessarily reduce single instruction latency

## ✅ Interview Answer

> Pipelining does not necessarily make one instruction faster; it increases throughput.


---

# 🚫 Pipeline Flush

A pipeline flush removes instructions currently inside the pipeline.

---

## Why It Happens

Usually due to:

* Wrong branch prediction
* Exceptions
* Interrupts

---

## Result

The CPU:

* Discards incorrect instructions
* Reloads correct ones

This wastes CPU cycles and reduces performance.

## ✅ Interview Answer

> A pipeline flush wastes cycles because the CPU must discard wrong-path instructions.



---

# 🔌 Logic Gates

Logic gates perform Boolean operations on binary values (`0` and `1`).

They are the basic building blocks of digital circuits.

---

# Common Logic Gates

| Gate | Function                        |
| ---- | ------------------------------- |
| AND  | True if both inputs true        |
| OR   | True if at least one input true |
| NOT  | Inverts input                   |
| XOR  | True if inputs differ           |
| NAND | Opposite of AND                 |
| NOR  | Opposite of OR                  |

---

## Example

### AND Gate

| A | B | Output |
| - | - | ------ |
| 0 | 0 | 0      |
| 0 | 1 | 0      |
| 1 | 0 | 0      |
| 1 | 1 | 1      |

---

## Important Point

Modern CPUs are built using billions of logic gates.

## ✅ Interview Answer

> Logic gates combine binary inputs to produce binary outputs according to Boolean logic.


---

# ⚖️ RAM vs ROM Quick Comparison

| Feature  | RAM             | ROM                |
| -------- | --------------- | ------------------ |
| Volatile | Yes             | No                 |
| Writable | Yes             | Usually No         |
| Purpose  | Active programs | Firmware/boot code |
| Speed    | Faster          | Slower             |

---

# ⚡ Cache vs RAM

| Feature  | Cache           | RAM         |
| -------- | --------------- | ----------- |
| Speed    | Faster          | Slower      |
| Size     | Smaller         | Larger      |
| Location | Near/inside CPU | Main memory |

---

# 🎯 Final Interview Tips

* Always explain why cache improves performance
* Mention that pipelining increases throughput
* Use “volatile vs non-volatile” when comparing memory
* Keep explanations simple and structured
* Use real-world examples like opening applications or booting a computer

---

# ⚡ Quick Revision Checklist

* [ ] CPU Instruction Cycle
* [ ] Registers
* [ ] Cache Memory
* [ ] Memory Hierarchy
* [ ] RAM
* [ ] ROM
* [ ] Pipelining
* [ ] Pipeline Flush
* [ ] Logic Gates

---

Good luck with your interview 🚀
