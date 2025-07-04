# POSIX
* Released in the late 1980s, POSIX (Portable Operating System Interface) is a family of standards created to make sure that applications developed on one UNIX flavor can run on other UNIXes.

## Copy On Write
* Copies the in memory data for a child process only when any of the processes makes a write operation on it

## File descriptors
* Keeps the list of open files and assigns a number to each of them
* Everything is a file in Linux (sockets, ports, files, shell commands, etc)

## Daemon
* A process running in the background with no user input required

## Process Table (Process Control Block)
* It contains an entry for each process in the system. The entry is created when a process is created by a fork system call.

# Orphan Process
* A process whose parent process has terminated and it is then re-parented by the init process
* If a parent process terminates before its child, the child becomes an orphan. The operating system typically re-parents the orphan to the init process (PID 1), which then becomes responsible for the orphan. The init process monitors the orphan and will eventually collect its exit status when the orphan terminates. 

## Zombie Process
* A process which has finished the execution but still has entry in the process table to report to its parent process is known as a zombie process. 
* A child process always first becomes a zombie before being removed from the process table.
* When a child process finishes, the kernel sends a signal to the parent process to inform it of the child's termination. If the parent doesn't read the exit status, the child becomes a zombie process. This can lead to resource leaks if many zombie processes accumulate because they are still taking up space in the process table. 
* The parent may be performing some other task due to which it was unable to get the exit signal from its child task

## Double Fork
* Create a child process which again creates a child, thus the new child becoming the grandchild of the original process. This grandchild process runs as a daemon
* The forked child process becomes the new session leader and can acquire a tty, hence it creates another child process and exits, thus creating an orphaned process which is reparented to init, and it becomes the init's responsibility to manage cleanup for this
* The main reason to do this is to handle daemon zombie processes that run in the background and keep consuming resources

## Teletype (TTY)
* In Linux, a TTY (teletype) refers to a character-based text interface for interacting with the operating system, also known as a terminal. 
* TTYs can be virtual, like the consoles accessed with Ctrl+Alt+Fn, or software terminals like terminal emulators within a graphical environment. The tty command prints the name of the terminal connected to standard input, confirming if the input is a terminal. 
* The shell runs on a TTY. 

## MMap 
* A system call that maps a file into memory
* This allows the process to read the file as if it were in memory

## Pages
* Blocks that the memory is organized into (usually 4kb)

## Thrashing
* When CPU spends more time context switching than actually working. 

## Unix Signals
* SIGHUP: Signal Hangup. Used for graceful restart of a process
* SIGTERM: Signal Terminate. Used for gracefully shutting down processes
* SIGQUIT: Signal Quit. Immediate shut down

## Preemptive Scheduling
* The operating system can interrupt or preempt a running process to allocate CPU time to another process, typically based on priority or time-sharing policies. Mainly a process is switched from the running state to the ready state. Algorithms based on preemptive scheduling are Round Robin (RR) , Shortest Remaining Time First (SRTF) , Priority (preemptive version) , etc.

## Non-Preemptive Scheduling
* In non-preemptive scheduling, a running process cannot be interrupted by the operating system; it voluntarily relinquishes control of the CPU. In this scheduling, once the resources (CPU cycles) are allocated to a process, the process holds the CPU till it gets terminated or reaches a waiting state.

The nc command, short for Netcat, is a versatile command-line utility in Linux and other Unix-like systems. It's used for reading and writing data across network connections using TCP or UDP. Essentially, it's a "Swiss Army knife" of network tools, useful for tasks like port scanning, file transfers, and even creating basic chat servers. 

## Fork
* It is a system call used to create a new process in Linux. 
* On failure, returns -1. Else returns the PID to the parent. It returns 0 to the child process

## Disown
* Shell command used to detach background process from the current shell session. In linux, it can also be done by appending a '&' to the command.

## IPC (Inter Process Communication)
* Way to communicate between processes (can be on different servers as well)
* Types of IPC
    * Shared Memory 
        * Creates a shared memory for 2 processes to use
        * This is faster than message passing since system call has to be made just once to create a shared memory, and then using the memory properly is the responsibility of the processes
    * Message Passing
        * Passed messages to the process using a queue separately created for message passing between the 2 processes
        * This process is slow since system calls need to be made for every message that has to be passed. System calls involve switching between user mode and kernel mode, which can slow down program execution.


## Program Counter
* A register within a CPU that keeps track of the memory address of the next instruction to be executed in a program. It essentially acts as a pointer to the next instruction, ensuring the CPU knows where to fetch the next piece of code to run. 

## Executable and Linkable Format (ELF)
* The Executable and Linkable Format(ELF, formerly named Extensible Linking Format) is a common standard file format for executable files, object code, shared libraries, and core dumps.

## 32 bit vs 64 bit Architectures
* The terms "32-bit" and "64-bit" primarily refer to the width of the registers in a computer's Central Processing Unit (CPU) and the size of the memory addresses that the CPU can handle
* A 32 bit cpu has registers that can hold 32 bits of data at a time, while a 64 bit cpu can hold 64 bits
* More bits means a CPI can process larger chunks of information in a single operation
* To access data in RAM, the CPU needs to know the memory address of the data. The number of bits are corelated with the maximum number of unique memory addresses the CPU can refer to
* 32 bit systems can directly access up to 2^32 bits of memory (4 GBs). That means 32 bit systems can only utilize a maximum of 4 GBs of RAM
* 64 bit systems can theoretically access up to 2^64 bits of memory (16 Exabytes).
* A 64 bit processor can handle more data in a single clock cycle compared to a 32 bit processor. This allows for faster processing of large datasets and more complex computations
* 64 bit systems can run for 32 bit and 64 bit softwares. On windows (x86) is used to define 32 bit programs

## Pointers
* A pointer takes 32 bits on a 32 bit system and 64 bits on a 64 bit system since it should be able to point to any of the 2^n combinations of memeory address in the system. That's why 32 bit programs can only point to 4GBs of location even if the RAM is more
* When we inspect the value inside a pointer, it is usually a hexadecimal number
* 0x prefix is used to signify it is a hexadecimal value (which is a convention)

## Clock Cycle
* A clock cycle, also known as a machine cycle or clock tick, is the fundamental unit of time in a computer's central processing unit (CPU). It represents a single, discrete operation of the CPU, involving tasks like fetching, decoding, executing, and storing instructions. The clock cycle's duration is determined by the clock signal's frequency, with a higher frequency meaning shorter clock cycles and faster processing. 
* A CPU's operation is synchronized by a clock signal, which is a regular, oscillating pulse. 
* The time between two consecutive rising or falling edges of the clock signal is the clock period or cycle time. 
* The clock frequency (measured in Hertz - Hz, typically MHz or GHz) is the inverse of the clock period, representing how many clock cycles occur per second.
* The CPU's speed is directly related to its clock frequency. A higher clock frequency means the CPU can perform more operations in a given time. 
*  Each clock cycle allows the CPU to perform a specific operation, such as fetching an instruction from memory, decoding it, executing it, and storing the result. 