# Time Sharing Operating Systems
## Introduction
Time-sharing operating systems enable multiple users to access and use multiple applications on a single computer system concurrently, using multiple processors and virtual machines. This is achieved through the sharing of resources, allowing several users to share one computer at the same time. Resources, such as memory space and processor cycle between applications so nobody has to wait for anything while another user is running an application.

## What is it?
A time-sharing operating system is software that allows multiple users to use the same computer at the same time. This type of system is used in computer networks and allows every user access to his or her own portion of the CPU. Time-sharing operating systems are also sometimes called multitasking or virtual machine environment (VME).

## History
The concept of a time-sharing computer was first described by IBM’s  [John Backus](https://www.ibm.com/history/john-backus "Story: John Backus")  at a summer session at MIT in 1955. Backus would go on to have a storied 41-year career at IBM and is best known as the father of  [Fortran](https://www.ibm.com/history/fortran "Story: Fortran"), the first widely used, high-level programming language that helped open the door to modern computing. But that was after his time-sharing revelation. “By time-sharing, a big computer could be used as several small ones; there would need to be a reading station for each user,” Backus postulated.

In the early 1960s, an experimental time-sharing system was launched at MIT on a modified IBM 709. MIT added a typewriter input so that an operator could obtain additional answers from the computer on a time-sharing basis with other programs accessing the machine simultaneously. The system, which became known as the Compatible Time-Sharing System (CTSS), was one of the first widely used time-sharing operating systems. Service to MIT users began in 1963 and remained in use until 1973.

## Working
   -   The CPU time is divided into small time slices and allocated to each user or process.
        
   -   The operating system switches rapidly between tasks, giving the illusion of simultaneous execution.
        
   -   A scheduler manages the execution of processes based on priority and fairness.
        
   -   User programs run in isolated virtual environments to prevent interference.
        
   -   If a process exceeds its allocated time slice, it is paused, and the next process gets CPU time.
        
   -   Memory and resources are dynamically allocated and managed to ensure efficiency.
        
   -   Input/output operations are scheduled to optimize system performance and responsiveness.

## Techniques Used 

### 1. CPU scheduling
-   The CPU scheduler allocates processing time to multiple users or virtual machines (VMs).
    
-   Each VM runs as an independent entity, and the scheduler ensures fair CPU distribution among them.
    
-   Time slices are assigned to each process or VM to maintain smooth multitasking.
    
-   If a VM or process exceeds its time slice, it is preempted, and the next in queue gets CPU access.
    
-   The scheduling algorithm (e.g., Round Robin, Priority Scheduling) determines the order of execution.
    
-   Virtual machine monitors (VMMs) manage CPU scheduling to ensure VMs do not interfere with each other.
    
-   Efficient CPU scheduling enhances resource utilization and ensures system stability.

### 2. Multitasking
-   Multitasking allows multiple programs to appear active at the same time through fast task switching.
    
-   In a time-sharing OS, multiple VMs or user processes share CPU resources efficiently.
    
-   For example, running Google Chrome and Spotify inside separate VMs does not mean they execute at the same time; the OS rapidly switches between them.
    
-   Virtual Machines manage their own tasks separately within the allocated CPU time slices.
    
-   Users can switch between applications using shortcuts like Ctrl+Tab or Alt+Tab, similar to switching between tasks in a VM environment.
    
-   Modern multitasking in time-sharing OS and VMs enhances efficiency by dynamically distributing computing power.
#### NOTE :  A single processor cannot execute multiple processes simultaneously; it switches between them rapidly.

### 3. Multi Programming
-   Multiple programs can run on a single computer
-   When the CPU is busy with one program, it doesn't have time for others
-   Programs can use different parts of the CPU simultaneously, each getting access when their turn comes
-   Analogy: Like three people in a car with separate seats and windows
    -   Each person can perform different activities (driving, reading)
    -   Each has their own space and limited interaction with others
    -   Communication only through specific channels (like text messages)
    
### 4. Parallel systems
-   Most common type of computer system
-   Use multiple processors to perform a single task
-   Advantages over serial processing:
    -   Greater flexibility in system resource usage
    -   Requires less hardware than serial systems
    -   Better performance with more processors (e.g., for large databases)
-   Cost considerations:
    -   Higher upfront costs due to more initial hardware
    -   Lower long-term costs through reduced maintenance and power consumption
### In the Context of Time-Sharing OS and Virtual Machines
-   Time-sharing OS allows multiple users/programs to share computing resources
-   CPU time is divided into slices allocated to different processes
-   Creates illusion that multiple programs run simultaneously
-   Virtual machines extend this concept by:
    -   Simulating complete hardware environments
    -   Allowing multiple OS instances to run on one physical machine
    -   Providing isolation between environments
    -   Enabling efficient resource allocation across applications

## Advantages
-   **Improved CPU Utilization**: Uses CPU time efficiently by switching between processes when one is waiting for I/O operations, preventing idle CPU time.
-   **Reduced Response Time**: Provides faster response to user interactions by allocating small time slices to each process, making the system feel responsive.
-   **Multiple User Support**: Allows several users to interact with the system simultaneously, maximizing hardware resource usage.
-   **Resource Sharing**: Enables users to share common resources like printers, storage, and software applications.
-   **Reduced Cost Per User**: Lowers the per-user cost of computing by distributing the cost of expensive hardware and software across multiple users.
-   **Increased Throughput**: Completes more processes in a given time period by minimizing CPU idle time.
-   **Interactive Computing**: Supports direct interaction between users and the system, providing immediate feedback to commands.
-   **Improved System Availability**: Maintains system accessibility even when some users experience problems, as each user operates in a separate process.
-   **Batch Processing Integration**: Can also handle background batch processing alongside interactive tasks.
-   **Efficient Memory Management**: Implements virtual memory techniques to run programs larger than available physical memory.
-   **Fair Resource Allocation**: Implements scheduling algorithms to ensure fair CPU time distribution among users and processes.
-   **System Monitoring and Management**: Provides tools for administrators to monitor system performance and manage resources effectively.

## Disadvantages
-   **Increased System Complexity**: Requires sophisticated memory management, CPU scheduling, and process management techniques.
-   **Performance Degradation with Load**: System performance decreases as the number of simultaneous users increases, leading to longer response times.
-   **Memory Constraints**: Limited physical memory can cause excessive swapping/paging when too many processes are active, resulting in "thrashing."
-   **Security Vulnerabilities**: Multiple users sharing the same system creates potential security risks and privacy concerns.
-   **Reliability Issues**: A single system failure affects all users simultaneously.
-   **Resource Contention**: Users compete for limited system resources, causing bottlenecks.
-   **Scheduling Overhead**: CPU time is consumed by the overhead of switching between processes.
-   **Complex Synchronization Requirements**: Multiple concurrent processes require careful synchronization to prevent race conditions and deadlocks.
-   **Data Integrity Challenges**: Simultaneous access to shared data requires complex locking mechanisms to maintain consistency.
-   **Higher Hardware Requirements**: Needs more powerful hardware than single-user systems to maintain acceptable performance.
-   **Maintenance Difficulties**: Troubleshooting is more complex due to the interaction of multiple concurrent processes.
-   **Inconsistent Response Times**: Users may experience variable response times depending on overall system load.
