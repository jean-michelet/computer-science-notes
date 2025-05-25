# OS

Some questions and exercises inspired by the content of the book [Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/) by Remzi Arpaci-Dusseau and Andrea C. Arpaci-Dusseau.

> I recommend opening a notebook and writing down your answers.
> This will help you structure your thoughts more clearly and avoid the illusion of knowledge by simply looking at the answer.

## Summary
- [Virtualization](#virtualization)

## Virtualization

**What is the main role of an operating system (OS)?**
<details><summary><b>Answer</b></summary>
<p>
The OS manages and allocates physical and virtual resources (CPU, memory, I/O devices) and provides an interface between hardware and user-level programs.
</p>
</details>

**What is the difference between a program and a process?**
<details><summary><b>Answer</b></summary>
<p>
A program is a binary file stored on disk; a process is an instance of that program loaded into memory and currently being executed by the CPU.
</p>
</details>

**What does the OS do when you run an executable file?**
<details><summary><b>Answer</b></summary>
<p>
The OS loads the binary into memory, sets up the process's execution environment (including code, stack, and heap), creates a Process Control Block (PCB), assigns it a unique Process ID (PID), and typically places the process in the ready queue to await scheduling.
</p>
</details>

**How does the OS give the illusion that each process has its own CPU?**
<details><summary><b>Answer</b></summary>
<p>
The OS uses a scheduler to time-slice CPU resources and perform context switching, rapidly switching between processes to create the illusion of concurrency.
</p>
</details>

**What are virtual addresses, and why does the OS use them?**
<details><summary><b>Answer</b></summary>
<p>
Virtual addresses are memory addresses used by processes, mapped to physical memory by the OS using the MMU. This allows isolation, memory protection, and more efficient memory use. Each process has its own virtual address space.
</p>
</details>

**What is the function of a device driver?**
<details><summary><b>Answer</b></summary>
<p>
A device driver is a specialized software module that allows the OS to communicate with a specific hardware device by providing a standard interface and abstracting hardware-specific operations.
</p>
</details>

**What’s the difference between a procedure call and a system call?**
<details><summary><b>Answer</b></summary>
<p>
A procedure call is a function call within user space. A system call is a request made by a program to the OS to perform privileged operations (e.g., file I/O, memory allocation), involving a switch from user mode to kernel mode.
</p>
</details>

**Imagine a program is running. Name and briefly explain the role of these elements: code segment, stack, heap, PC, and registers.**
<details><summary><b>Answer</b></summary>
<p>

- **Code Segment**: Contains the executable machine instructions. Usually read-only.
- **Stack**: Used for managing function calls and storing local variables. Automatically managed (push/pop).
- **Heap**: Used for dynamic memory allocation. Manually managed by the programmer (e.g., `malloc`/`free` in C).
- **Program Counter (PC)**: A CPU register that stores the address of the next instruction to execute.
- **Registers**: Small fast storage in the CPU used for intermediate calculations and execution control.

</p>
</details>

**Describe what happens, step by step, when you type `./a.out` in a terminal and press Enter.**
<details><summary><b>Answer</b></summary>
<p>

1. The terminal passes the command to the OS.
2. The OS loads the binary into memory.
3. It sets up the process’s environment (code, stack, heap, etc.).
4. A PCB (Process Control Block) is created and a PID is assigned.
5. The process is placed into the ready queue.
6. The CPU scheduler eventually picks the process to run, and execution begins.

</p>
</details>

**Suppose you are running two programs: a web browser and a text editor. Both are using the same memory address. Explain why that’s not a problem.**
<details><summary><b>Answer</b></summary>
<p>
Each process runs in its own isolated virtual address space. The memory address in the browser maps to a different physical location than the one in the text editor, thanks to virtual memory and the MMU.
</p>
</details>

**Consider this simple C code:**

```c
printf("Hello\n");
```

_Is `printf` a system call?_
<details><summary><b>Answer</b></summary>
<p>
  
No, `printf` is a standard C library function that handles formatting and buffering. It is not a direct system call.

</p>
  
</details>

_If not, which part of this operation involves a system call?_
<details><summary><b>Answer</b></summary>
<p>
The actual output to the terminal involves a system call performing low-level I/O operation via the OS.
</p>
</details>

[⬆️ Return to top](#summary)
