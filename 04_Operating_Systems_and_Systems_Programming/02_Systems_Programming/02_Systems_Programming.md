# Systems Programming 

### Key Topics and Notes
- [Introduction to Unix and Linux Systems MOC](./00_MOCs/01_Introduction_to_Unix_and_Linux_Systems_MOC.md)
- [File I/O and System Calls MOC](./00_MOCs/02_File_IO_and_System_Calls_MOC.md)
- [Processes and Process Management MOC](./00_MOCs/03_Processes_and_Process_Management_MOC.md)
- [Memory Management and Allocation MOC](./00_MOCs/04_Memory_Management_and_Allocation_MOC.md)
- [User and Group Management MOC](./00_MOCs/05_User_and_Group_Management_MOC.md)
- [Time and Scheduling MOC](./00_MOCs/06_Time_and_Scheduling_MOC.md)
- [Signals and Signal Handling MOC](./00_MOCs/07_Signals_and_Signal_Handling_MOC.md)
- [Interprocess Communication IPC MOC](./00_MOCs/08_Interprocess_Communication_IPC_MOC.md)
- [Sockets and Networking MOC](./00_MOCs/09_Sockets_and_Networking_MOC.md)
- [Threading and Concurrency MOC](./00_MOCs/10_Threading_and_Concurrency_MOC.md)
- [Security and Privileged Programming MOC](./00_MOCs/11_Security_and_Privileged_Programming_MOC.md)
- [System Resources and Limits MOC](./00_MOCs/12_System_Resources_and_Limits_MOC.md)
- [Daemons and System Monitoring MOC](./00_MOCs/13_Daemons_and_System_Monitoring_MOC.md)


## Resources
- [Advanced Programming UNIX, W. Richard Stevens](./01_Resources/Advanced_Programming_UNIX_Richard.pdf)
- [The Linux Programming Interface, Michael Kerrisk](./01_Resources/The_Linux_Programming_Interface_Michael.pdf)
- [System Programming Resources and Examples](./02_Resources/System_Programming_Examples.pdf)

## Progress
### Foundations
- [ ] Introduction to Unix and Linux Systems  
- [ ] File I/O and System Calls  

### Core Concepts  
- [ ] Processes and Process Management  
- [ ] Memory Management and Allocation  
- [ ] User and Group Management  

### Advanced Topics  
- [ ] Signals and Signal Handling  
- [ ] Interprocess Communication (IPC)  
- [ ] Threading and Concurrency  

### Specialized Topics  
- [ ] Security and Privileged Programming  
- [ ] Sockets and Networking  
- [ ] Daemons and System Monitoring  

---

## Syllabus

### 1. Introduction to Unix and Linux Systems (Weeks 1-2)
- **Topics**:  
  - History of Unix and Linux  
  - System Architecture and Operating Systems Overview  
  - Shells and Terminal Interaction  
  - Basic File System Hierarchy  
  - Process Management Fundamentals  
- **Practice**: Use shell commands to navigate the file system, explore system calls  
- **Applications**: Linux system administration, Unix philosophy  

---

### 2. File I/O and System Calls (Weeks 3-4)
- **Topics**:  
  - The Universal I/O Model  
  - Basic File Operations (Open, Read, Write, Close)  
  - Advanced File Operations (Seek, Truncate, Sync)  
  - System Calls for File I/O  
  - Error Handling in System Calls  
- **Practice**: Implement file handling operations using system calls  
- **Applications**: File system programming, system-level I/O  

---

### 3. Processes and Process Management (Weeks 5-6)
- **Topics**:  
  - Process Creation and Termination  
  - Process Control Block and Process States  
  - Forking and Executing Programs  
  - Process ID and Parent-Child Relationship  
  - Waiting and Exiting Processes  
- **Practice**: Implement process creation and management using `fork()` and `exec()`  
- **Applications**: System-level application development, multitasking  

---

### 4. Memory Management and Allocation (Weeks 7-8)
- **Topics**:  
  - Memory Models and Allocation Strategies  
  - Dynamic Memory Allocation and Deallocation  
  - Memory Mapping and Shared Memory  
  - Virtual Memory Concepts  
  - Paging and Segmentation  
- **Practice**: Write programs utilizing dynamic memory allocation  
- **Applications**: Performance optimization, memory management techniques  

---

### 5. User and Group Management (Weeks 9-10)
- **Topics**:  
  - User and Group Creation  
  - Managing User Permissions and Privileges  
  - File Ownership and Access Control  
  - Understanding the `/etc/passwd` and `/etc/group` Files  
- **Practice**: Set up and modify user permissions, manage groups  
- **Applications**: Security administration, user-based access control  

---

### 6. Time and Scheduling (Weeks 11-12)
- **Topics**:  
  - Time Representation in Unix  
  - System Time and Clock Management  
  - Scheduling Algorithms and Priorities  
  - Time-related System Calls (Sleep, Alarm)  
- **Practice**: Implement time-sensitive applications  
- **Applications**: Process scheduling, time management in systems  

---

### 7. Signals and Signal Handling (Weeks 13-14)
- **Topics**:  
  - Understanding Signals and Signal Handling  
  - Setting Up Signal Handlers  
  - Signal Masking and Blocking  
  - Advanced Signal Management (SIGSEGV, SIGKILL)  
- **Practice**: Write programs that handle Unix signals  
- **Applications**: Robust process handling, real-time application programming  

---

### 8. Interprocess Communication (IPC) (Weeks 15-16)
- **Topics**:  
  - Overview of IPC Methods  
  - Pipes and FIFOs  
  - System V IPC (Message Queues, Semaphores, Shared Memory)  
  - POSIX IPC (Message Queues, Semaphores, Shared Memory)  
  - Sockets for IPC  
- **Practice**: Develop applications using different IPC methods  
- **Applications**: Multitasking, distributed systems, client-server programming  

---

### 9. Threading and Concurrency (Weeks 17-18)
- **Topics**:  
  - Threads vs Processes  
  - Creating and Managing Threads  
  - Synchronization Techniques (Mutexes, Semaphores)  
  - Thread Safety and Race Conditions  
  - Thread Scheduling and Management  
- **Practice**: Implement multi-threaded applications, handle concurrency issues  
- **Applications**: High-performance systems, parallel computing  

---

### 10. Security and Privileged Programming (Weeks 19-20)
- **Topics**:  
  - Writing Secure Code and Avoiding Vulnerabilities  
  - Privileged Programs and Capabilities  
  - User Authentication and Authorization  
  - Securing File Systems and Data  
- **Practice**: Develop programs with focus on security and safe practices  
- **Applications**: Secure system design, application security  

---

### 11. Sockets and Networking (Weeks 21-22)
- **Topics**:  
  - Introduction to Sockets Programming  
  - TCP and UDP Sockets  
  - Client-Server Architecture  
  - Internet Sockets and Network Communication  
  - Handling Network Errors  
- **Practice**: Write socket-based networked applications  
- **Applications**: Web servers, networked applications  

---

### 12. Daemons and System Monitoring (Weeks 23-24)
- **Topics**:  
  - Creating Daemon Processes  
  - System Logs and Monitoring Tools  
  - Process Control and Job Scheduling  
  - Debugging and Profiling System Programs  
- **Practice**: Write daemon processes, set up monitoring tools  
- **Applications**: System administration, automation  

---

### 13. Advanced Topics and Resources (Weeks 25-26)
- **Topics**:  
  - Advanced File Systems (Ext4, XFS)  
  - Advanced Network Programming  
  - Linux Kernel and System Programming  
  - Case Studies and Real-World System Programming Challenges  
- **Practice**: Study real-world case studies, build advanced system applications  
- **Applications**: Operating system development, large-scale system design  

----e 

---
**Up to:** [[Index]]
