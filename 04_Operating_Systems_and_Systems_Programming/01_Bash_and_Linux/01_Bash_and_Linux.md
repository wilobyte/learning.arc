
# Bash and Linux 

### Key Topics and Notes
- [Command Line Basics MOC](./00_MOCs/01_Command_Line_Basics_MOC.md)
- [Shell Scripting MOC](./00_MOCs/02_Shell_Scripting_MOC.md)
- [File Management MOC](./00_MOCs/03_File_Management_MOC.md)
- [Process Management MOC](./00_MOCs/04_Process_Management_MOC.md)
- [User and Permissions Management MOC](./00_MOCs/05_User_and_Permissions_Management_MOC.md)
- [Networking MOC](./00_MOCs/06_Networking_MOC.md)
- [Package Management MOC](./00_MOCs/07_Package_Management_MOC.md)
- [System Boot and Initialization MOC](./00_MOCs/08_System_Boot_and_Initialization_MOC.md)
- [Text Processing MOC](./00_MOCs/09_Text_Processing_MOC.md)
- [Regular Expressions MOC](./00_MOCs/10_Regular_Expressions_MOC.md)
- [File System Hierarchy MOC](./00_MOCs/11_File_System_Hierarchy_MOC.md)
- [Environment Variables and Configuration Files MOC](./00_MOCs/12_Environment_Variables_and_Configuration_Files_MOC.md)
- [Advanced Shell Features MOC](./00_MOCs/13_Advanced_Shell_Features_MOC.md)
- [Debugging and Troubleshooting MOC](./00_MOCs/14_Debugging_and_Troubleshooting_MOC.md)

## Resources  
- [Ebook: The Linux Command Line, William E. Shotts, Jr.](./01_Resources/01_The_Linux_Command_Line_Shotts.pdf)  
- [Ebook: Linux Pocket Guide, Daniel J. Barrett](./01_Resources/02_Linux_Pocket_Guide_Barret.pdf)  
- [Ebook: Bash Cookbook, Carl Albing](./01_Resources/03_Bash_Cookbook_Albing.pdf)  
- [Practice Problems](./02_Practice-Problems.md)  
- [Command Line Reference](./01_Resources/CommandLineReference.pdf)

## Progress  
### Foundations  
- [ ] Command Line Basics  
- [ ] File Management  

### Core Concepts  
- [ ] Shell Scripting  
- [ ] Process Management  
- [ ] User and Permissions Management  

### Advanced Topics  
- [ ] Networking  
- [ ] Advanced Shell Features  
- [ ] Debugging and Troubleshooting  

---

## Syllabus  

### 1. Command Line Basics (Weeks 1-2)  
- **Topics**:  
  - Introduction to the Terminal  
  - Navigating the File System (cd, ls, pwd)  
  - File and Directory Structure  
  - Basic Commands (cp, mv, rm, mkdir, touch)  
  - Viewing File Content (cat, less, more, head, tail)  
  - Understanding Paths (Absolute and Relative)  
- **Practice**: Execute basic commands and explore the file system  
- **Applications**: General system navigation, troubleshooting  

---

### 2. File Management (Weeks 3-4)  
- **Topics**:  
  - File Permissions (chmod, chown, chgrp)  
  - Ownership and Access Control Lists (ACLs)  
  - File Compression and Archiving (tar, gzip, zip)  
  - Symlinks and Hard Links  
  - Finding Files (find, locate, which)  
  - Disk Usage and Filesystems (du, df, mount)  
- **Practice**: Manage files and directories efficiently  
- **Applications**: File organization, backup processes  

---

### 3. Shell Scripting (Weeks 5-6)  
- **Topics**:  
  - Writing Basic Shell Scripts  
  - Variables and Environment Variables  
  - Conditional Statements (if, else, elif)  
  - Loops (for, while)  
  - Functions and Parameters  
  - Error Handling and Exit Statuses  
  - Scripting Best Practices  
- **Practice**: Write simple shell scripts for automation  
- **Applications**: Task automation, system administration  

---

### 4. Process Management (Weeks 7-8)  
- **Topics**:  
  - Viewing Processes (ps, top, htop)  
  - Process Management (kill, pkill, killall)  
  - Job Control (bg, fg, jobs)  
  - Understanding Process States (sleep, running, stopped)  
  - Managing System Resources (nice, renice, ulimit)  
- **Practice**: Manage and monitor system processes  
- **Applications**: System administration, performance tuning  

---

### 5. User and Permissions Management (Weeks 9-10)  
- **Topics**:  
  - Creating and Managing Users (useradd, userdel, passwd)  
  - Groups and Group Management  
  - File Permissions and Ownership  
  - Sudo and Administrative Privileges  
  - Security Best Practices  
  - Scripting User Management  
- **Practice**: Configure user accounts and permissions  
- **Applications**: User and group management, system security  

---

### 6. Networking (Weeks 11-12)  
- **Topics**:  
  - Basic Networking Commands (ping, ifconfig, netstat, ip)  
  - Configuring Network Interfaces  
  - SSH for Remote Access  
  - Managing Network Connections (wget, curl)  
  - Network Troubleshooting (traceroute, nslookup)  
- **Practice**: Configure networking and troubleshoot connectivity  
- **Applications**: Remote management, network diagnostics  

---

### 7. Package Management (Weeks 13-14)  
- **Topics**:  
  - Installing and Updating Packages (apt, yum, dnf, pacman)  
  - Package Management Tools (dpkg, rpm)  
  - Searching for Packages  
  - Managing Repositories  
  - Package Dependencies  
- **Practice**: Install and manage packages on various Linux distributions  
- **Applications**: Software installation, system maintenance  

---

### 8. System Boot and Initialization (Weeks 15-16)  
- **Topics**:  
  - Boot Process and BIOS/UEFI  
  - GRUB and Boot Loaders  
  - Init Systems (SysVinit, Upstart, systemd)  
  - Managing Services and Daemons (systemctl)  
  - Boot Time and Shutdown Procedures  
- **Practice**: Understand and configure boot systems  
- **Applications**: Troubleshooting, system optimization  

---

### 9. Text Processing (Weeks 17-18)  
- **Topics**:  
  - Working with Text Files (cat, grep, awk, sed)  
  - Pattern Matching and Regular Expressions  
  - Text Filters (sort, uniq, tr)  
  - Processing Large Files  
  - Piping and Redirection  
- **Practice**: Write text processing scripts  
- **Applications**: Data extraction, log analysis  

---

### 10. Regular Expressions (Weeks 19-20)  
- **Topics**:  
  - Introduction to Regular Expressions  
  - Basic Syntax and Metacharacters  
  - Regular Expressions in grep, sed, and awk  
  - Advanced Regular Expressions (lookaheads, backreferences)  
  - Practical Applications of Regex  
- **Practice**: Create and test regular expressions  
- **Applications**: Data manipulation, log parsing  

---

### 11. File System Hierarchy (Weeks 21-22)  
- **Topics**:  
  - Linux Directory Structure  
  - Understanding File System Standards (FHS)  
  - Mounting and Unmounting File Systems  
  - Filesystem Types (ext4, XFS, Btrfs)  
  - Disk Partitioning and RAID  
- **Practice**: Explore and manage filesystems  
- **Applications**: Disk management, file organization  

---

### 12. Advanced Shell Features (Weeks 23-24)  
- **Topics**:  
  - Shell Customization (.bashrc, .bash_profile)  
  - Advanced Command Line Tools (xargs, tee)  
  - Creating and Using Aliases  
  - Shell Variables and Arrays  
  - Debugging Shell Scripts  
- **Practice**: Optimize the shell environment for productivity  
- **Applications**: Shell environment customization, script debugging  

---

### 13. Debugging and Troubleshooting (Weeks 25-26)  
- **Topics**:  
  - Log Files and Log Management  
  - System Logs (syslog, dmesg, journalctl)  
  - Error Reporting and Diagnosis  
  - Using strace and lsof  
  - Memory Management and Debugging Tools  
- **Practice**: Debug issues and analyze log files  
- **Applications**: System diagnostics, performance troubleshooting-e 

---
**Up to:** [[Index]]
