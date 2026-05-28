# 01-01-Intro_To_The Terminal

**Date:** 2025-06-06  
**Subject:** Operating Systems and Systems Programming  
**Parent MOC:** [[01_Command_Line_Basics_MOC]]  
**Topic:** Intro to the Terminal
**Source / Reference:**   Intro Chap, [The Linux Command Line, William E. Shotts, Jr.](/01_Resources/01_The_Linux_Command_Line_Shotts.pdf)

---

## Learning Objectives  
- Understand the basic overview and philosophy of Linux.
- Command line intro and terminology. 

---

## Concepts and Definitions  
- GUI(Graphical User Interface)
- CLI(Command Line Interface) 
- Linux is modelled after the UNIX family of operating systems.
- UNIX was an earlier system in the late 60's and focused on the development of robust command line tools instead of the GUI boom happening with systems like Windows NT.
- Linux is the name of the OS's kernel.
- The kernel makes the OS 'go'.
- The GNU ("GNU's Not UNIX") Project is where Linux came from. The project is for the Free Software foundation founded by Richard Stallman.
- Linux/GNU is a more technically accurate name (as opposed to GNU/Linux) since the 'Kernel' boots first and everything runs on top of it.
- Linux generally refers to the kernel and all the other free and open source software found in the typical Linux distribution(distro) i.e the entire Linux ecosystem, not just the GNU components.
- When we speak of the command line we're really referring to the **shell**.
- The shell is a program that passes commands from the keyboard to the operating system to execute.
- The shell from the GNU project used in almost every linux distro is called **bash**. 
- **bash** stands for the 'bourne again shell' and is an enhancement of UNIX's **sh** shell which was written by Steve Bourne. 
- When using a GUI you need a program to access the shell. This is called a **terminal emulator**.
- When you first open your terminal emulator you should get the **shell prompt** (check commands/code snippets).
- The anatomy of your shell prompt is usually username@machinename, your current working directory then a dollar sign($).
- If the last character is a hashtag(#) instead of a dollar sign, the terminal session has root/superuser privileges. This means we're either logged in as a root user or we opened a terminal emulator that has superuser privileges.

--- 
## Commands / Code Snippets  

- This is called a **shell prompt**, it appears whenever the shell is ready to accept input.
```bash
[wilobyte@wilobyte-pc ~]$ 
```

- Generally if you type a command that doesn't exist or isn't installed it'll show this error:
```bash
[wilobyte@wilobyte-pc ~]$ jljkljinilljlj
-bash: jljkljinilljlj: command not found
```

- The `date` command displays the current date and time.
```bash
[wilobyte@wilobyte-pc ~]$ date
Thu Jun 12 06:43:51 PM WAT 2025
```

- `cal` displays the calendar of the current month.
```bash
[wilobyte@wilobyte-pc ~]$ cal
	June 2025
Su Mo Tu We Th Fr Sa
 1  2  3  4  5  6  7
 8  9 10 11 12 13 14
15 16 17 18 19 20 21
22 23 24 25 26 27 28
29 30
```

- `df`  displays the current amount of free disk space:
```bash
[wilobyte@wilobyte-pc ~]$ df
Filesystem     1K-blocks     Used Available Use% Mounted on
/dev/sda6       98141608 28074408  65035668  31% /
devtmpfs            4096        0      4096   0% /dev
tmpfs            4018976    11436   4007540   1% /dev/shm
efivarfs             124       51        69  43% /sys/firmware/efi/efivars
tmpfs            1607592     1588   1606004   1% /run
tmpfs               1024        0      1024   0% /run/credentials/systemd-journald.service
tmpfs            4018976        8   4018968   1% /tmp
/dev/sda5        2093040   122480   1970560   6% /efi
tmpfs             803792      104    803688   1% /run/user/1002
```

- `free` displays the total amount of free memory:
```bash
[wilobyte@wilobyte-pc ~]$ free
               total        used        free      shared  buff/cache   available
Mem:         8037952     2788816     3712400      299696     2096012     5249136
Swap:              0           0           0
```

- To close a terminal window simply close it or type 'exit' in the shell prompt:
```bash
[wilobyte@wilobyte-pc ~]$ exit
```
---

## System Behavior and Examples  
- If you press the up arrow key the former command appears. This is called the command history and bash by default keeps the last 500 commands. Press the down arrow key and the previous command disappears.
- The left and right arrow keys allow the cursor to be positioned anywhere on the command line. This makes editing easier.
- Setting 'focus follows mouse' helps better in terminal management because when we simply move the mouse over a window it'll select that window even if it's in the background and we can't see it.

---
## Questions / Review Points  
- What are kernels exactly?
- How was Linux built and why does there seem to be a divide with the GNU community? 
- What is UNIX and how does it differ from Linux?

---
## Answers to Review Points
### - What are kernels exactly?
The kernel is an important part of the OS that handles direct communication and management of the hardware (CPU, memory, devices) to the software components of the system. It's generally kept separately/isolated and separates the system processes from user apps.
### - How was Linux built and why does there seem to be a divide with the GNU community? 
Basically, Linux is the free kernel made by Linus Torvalds in 1991, and based off the UNIX OS. The GNU tools are what make the kernel part of a complete OS so it's often called GNU/Linux.  Also it seems Linux is not extremely (though it's generally within the standards) compliant with GNU'S Free Software philosophy, adding more of a slight divide. 
### - What is UNIX and how does it differ from Linux?
Basically, UNIX is what Linux was based on as already mentioned. The OS was developed by AT&T Bell Labs in the late 60's. It was based on CLI  just like how the Linux kernel is today. Linux is based on UNIX but doesn't use any code from it. Linux is it's own whole, separate project, just with some inspiration from UNIX.
## Links to Related Notes  
- [[01_Command_Line_Basics_MOC]]  

---

## Tags  
#operatingsystems #intro_to_the_terminal #bash #to-review
