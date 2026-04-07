# Operating Systems Projects

## 🛠 Project 1: Shell Scripting, Synchronization & Memory Management

This project is divided into three core modules:

### 1. Shell Scripting (`processes_ipc.sh`)
Development of an automated script for managing passenger data (via `.csv` files or manual input).
* **Search & Filter:** Advanced data retrieval with case-insensitive filtering.
* **Data Manipulation:** Update records based on unique IDs or names.
* **Statistical Reporting:** Generation of reports including age demographics, survival rates, and average age of crew vs. passengers using `awk`, `sed`, and `grep`.

### 2. Process Synchronization with Semaphores
A simulation of a ship evacuation and lifeboat boarding procedure.
* **Implementation:** Windows API (`winbase.h`).
* **Logic:** Utilizing semaphores to manage lifeboat capacity and synchronize passenger processes to prevent race conditions.

### 3. Scheduling & Memory Management
A custom simulator that combines CPU scheduling and memory allocation:
* **Algorithm:** Round Robin (RR) with a 3ms time quantum.
* **Memory:** Static allocation (512 KB total) featuring block splitting during allocation and deallocation upon process completion.

---

## ⚙️ Project 2: Multi-Processor Scheduling

This project focuses on modifying a kernel-level scheduler to support multi-processor architectures.

### Phase A: FCFS in a Multi-Processor Environment
* **Resource Management:** Introduced variables for `total_processors` and `available_processors`.
* **Parallel Execution:** Modified the **First-Come, First-Served (FCFS)** algorithm to execute multiple processes simultaneously based on available CPU cores.
* **Process Tracking:** Implemented `waitpid` with the `WNOHANG` flag for non-blocking status checks.

### Phase B: Process-Specific Processor Requirements
* **Requirement Analysis:** Each process requests a specific number of cores (`processors_required`).
* **Resource Validation:** The scheduler dynamically checks if the available hardware meets the process demands.
* **Queue Management:** If resources are insufficient, the process is moved to the end of the Ready Queue (non-blocking) to optimize system throughput and prevent starvation.

---

## 💻 Technologies & Tools
* **Languages:** C, Bash Scripting.
* **Command Line:** Linux Utilities (`sed`, `awk`, `grep`).
* **Compilers:** GCC.
* **APIs:** Windows API (for synchronization primitives).
* **Operating Systems:** Linux (Shell & Scheduling), Windows (Semaphores).
