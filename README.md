# MemForge

**MemForge** is a C/C++ memory management simulator that models paging, virtual memory, process management, page tables, memory swapping, and LRU-based page replacement.

The system simulates the interaction between **main memory and virtual memory** and provides a command-based interface for loading, executing, swapping, terminating, and inspecting processes.

## 🚀 Features

* Memory allocation for processes
* Paging system implementation
* Virtual memory management
* Process execution simulation
* Memory swapping (swap-in and swap-out)
* Page table management
* LRU (Least Recently Used) page replacement
* Physical memory inspection

---

## 🛠 Key Components

1. **Memory Initialization**
   Initializes main memory and virtual memory based on the supplied memory and page-size parameters.

2. **Process Management**
   Handles loading, execution, and termination of processes.

3. **Paging System**
   Implements page tables and manages page allocation between memory pages and frames.

4. **Virtual Memory Handling**
   Manages the movement of processes between main memory and virtual memory.

5. **LRU Page Replacement**
   Uses the Least Recently Used strategy when main memory does not have sufficient free space.

6. **Command Interpreter**
   Reads and executes commands for managing processes and memory.

---

## 💻 Supported Commands

| Command                                        | Description                                |
| ---------------------------------------------- | ------------------------------------------ |
| `load <filename1> <filename2> ... <filenameN>` | Load executables into memory               |
| `run <pid>`                                    | Execute a process                          |
| `kill <pid>`                                   | Terminate a process                        |
| `listpr`                                       | List processes in main and virtual memory  |
| `pte <pid> <file>`                             | Print page table entries for a process     |
| `pteall <file>`                                | Print page table entries for all processes |
| `swapout <pid>`                                | Move a process to virtual memory           |
| `swapin <pid>`                                 | Move a process to main memory              |
| `print <memloc> <length>`                      | Print values from physical memory          |
| `exit`                                         | Terminate the system                       |

---

## ⚙️ Implementation Details

* **Language:** C/C++
* **Memory Model:** Paging with main and virtual memory
* **Page Replacement:** LRU (Least Recently Used)
* **Process Management:** Process loading, execution, swapping, and termination
* **Execution Support:** Basic `load`, `add`, `sub`, and `print` operations

---

## 📁 Project Structure

```text
MemForge/
│
├── main.cpp
├── Process.cpp
├── Process.h
├── MemoryManager.cpp
├── MemoryManager.h
└── README.md
```

---

## ▶️ Usage

### Compilation

```bash
g++ -o memoryEngine main.cpp Process.cpp MemoryManager.cpp
```

### Execution

```bash
./memoryEngine -M <main_memory_size> -V <virtual_memory_size> -P <page_size> -i <input_file> -o <output_file>
```

### Example

```bash
./memoryEngine -M 4 -V 8 -P 1 -i input -o output
```

---

## 🧠 Concepts Demonstrated

MemForge demonstrates several fundamental operating-system concepts:

* Virtual memory
* Paging
* Page tables
* Memory allocation
* Process management
* Swapping
* LRU page replacement
* Physical and virtual address translation
* Command-based process execution

---

## 📌 Project Goal

The goal of MemForge is to provide a practical simulation of how an operating system manages processes and memory using paging, virtual memory, page tables, and page replacement strategies.
