# FOS Operating System

An educational Operating System project developed as part of the curriculum at **Faculty of Computer and Information Sciences, Ain Shams University**. This project involves implementing core OS components including Memory Management, Process Scheduling, and Fault Handling.

---

## Table of Contents
* [Project Overview](#project-overview)
* [Team & Timeline](#team--timeline)
* [My Contributions](#my-contributions)
    * [1. Dynamic Allocator (Group Module)](#1-dynamic-allocator-group-module)
    * [2. Fault Handler II (Individual Module)](#2-fault-handler-ii-individual-module)
* [Technologies Used](#technologies-used)
* [Key Features Implemented](#key-features-implemented)

---

## Project Overview
FOS is a microkernel-based operating system. The project focuses on building the kernel's essential services from scratch. It is divided into several modules starting from prerequisite kernel heap management up to advanced page replacement policies and CPU scheduling.

---

## Team & Timeline
* **Team Size:** 6 Members.
* **Duration:** Oct 13, 2025 – Dec 6, 2025.
* **Institution:** Ain Shams University, Faculty of Computer and Information Sciences.

---

## My Contributions

I was responsible for critical parts in both the Group and Individual modules, focusing heavily on **Memory Management Strategies**.

### 1. Dynamic Allocator (Group Module)
Implemented a custom dynamic memory allocator to manage memory blocks efficiently.
* **`initialize_dynamic_allocator`**: Developed the logic to initialize the allocator with a specific range, setting up free block lists and free page tracking.
* **`alloc_block`**: Implemented the core allocation logic using a **Buddy System** or **Power-of-Two** approach to find/split blocks based on the requested size, ensuring optimal memory utilization.

### 2. Fault Handler II (Individual Module)
Worked on advanced Page Replacement Algorithms to manage memory under pressure.
* **LRU Aging Replacement**: Implemented the "Least Recently Used" approximation using aging bits.
    * **`update_WS_time_stamps`**: Logic to shift time stamps and track page usage every quantum.
    * **Replacement Logic**: Finding the victim page with the minimum timestamp to swap out.
* **Modified Clock Replacement**: Implemented an efficient 4-pass clock algorithm that considers both the `Used` and `Modified` bits to prioritize replacing non-modified pages (to avoid unnecessary disk writes).

---

## Technologies Used
* **Language:** C (Kernel Level)
* **Tools:** QEMU Emulator, GDB Debugger, Git/GitHub.
* **Concepts:** Virtual Memory, Paging, Segmentation, Kernel Structures, Interrupt Handling.

---

## Key Features Implemented
* **Kernel Heap Management:** Dynamic allocation and deallocation within the kernel.
* **Working Set Management:** Tracking and managing pages currently used by environments (processes).
* **Page Replacement:** Efficiently swapping pages between Physical RAM and Disk (Page File).
* **Hardware Abstraction:** Interacting with page tables and page directories.

---
