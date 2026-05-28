# 01-02-Navigating_The_File_System

**Date:** 2025-07-31  
**Subject:** Operating Systems and Systems Programming  
**Parent MOC:** [[01_Command_Line_Basics_MOC]]  
**Topic:** {{topic}}  
**Source / Reference:** [The linux command line, shotts](obsidian://open?vault=learning.arc&file=04_Operating_Systems_and_Systems_Programming%2F01_Bash_and_Linux%2F01_Resources%2F01_The_Linux_Command_Line_Shotts.pdf)

---

## Learning Objectives  
-  `pwd` - Print name of the current working directory.
- `cd` - Change directory.
- `ls` - List directory contents.

---

## Concepts and Definitions  
- ### The Filesystem Tree
	- A UNIX-like operating system such as Linux organizes it's files in what is called a *hierarchical directory structure*. This means they are organized in a tree-like pattern of directories (sometimes called folders in other operating systems), which may contain files and other directories.
	- The first directory in the filesystem is called the *root directory*. It contains files and subdirectories which contain other files and subdirectories and so on.
	- Unlike Windows which has a separate file tree for each storage device, UNIX-like systems such as Linux have a single file tree no matter how many storage devices are attached to the computer. Storage devices are attached (or more correctly *mounted*) at various points in the tree according to the way the system administrator (person(s) in charge of maintenance of the system) prefers it.
- ### The Current Working Directory
	- Imagine the filesystem as a tree with the 'root' at the top gradually spreading downwards. At any given time we are in a single directory and we can see the directory above us (the *parent directory*) and any subdirectories below us. The directory we are currently in is called the *current working directory*. 
	- To display the current working directory, we use the `pwd` command as shown below:
		```bash
		[wilobyte@wilobyte-hp ~]$ pwd
		/home/wilobyte
		```
	- When we first log in to our system (or start a terminal session), the current working directory we're placed in is our *home directory* by default. Every user account has a home directory which is the only place allowed to write files as a regular user.
- ### Listing the Contents of a Directory
	- To list the files and directories in the current working directory, we use the `ls` command as shown below:
		```bash
		[wilobyte@wilobyte-hp ~]$ ls  
		Desktop     Downloads   Pictures   python   Templates  'VirtualBox VMs' Documents   Music       Public     tagainijisho   Videos
		```
	- We can also use the `ls` command to list the contents of any directory, not just the current working directory.
- ### Changing the Current Working Directory
	- To change your current working directory, use the `cd` command followed by the pathname of the desired working directory.
	- A *pathname*, is a route we take along the branches of the tree to get to the directory you want. Pathnames can be specified in two ways: absolute or relative.
	- #### Absolute Pathnames
		- An *absolute pathname* begins with the root directory and follows the tree branch by branch until the path to the desired directory or file is completed.
		- For example, the directory where most of the system's programs are installed is refered to by the absolute pathname: `/usr/bin`. This means it starts from the root directory (represented by the leading slash in the pathname), goes into the subdirectory `usr` in the root directory, and goes to `bin` which is a subdirectory found in the `usr` directory.
	- #### Relative Pathnames
		- Instead of starting from the root directory like an absolute pathname, a *relative pathname* starts from the working directory. To do this it uses some special symbols to represent relative positions in the filesystem. These special symbols are `.` (dot) and `..` (dot dot).
		- The `.` symbol refers to the current working directory while the `..` symbol refers to the current working directory's parent directory.
		- For example let's say we are located in the `/usr/bin` directory and we want to move to it's parent directory `/usr`. To do this we could use the `cd /usr` but using the relative pathname symbols:
			```shell
			[wilobyte@wilobyte-hp bin]$ pwd  
			/usr/bin  
			[wilobyte@wilobyte-hp bin]$ cd ..  
			[wilobyte@wilobyte-hp usr]$ pwd  
			/usr
			```
		- Like wise, we could change the working directory from `/usr` to `/usr/bin` in two different ways; either by using it's absolute filename `cd /usr/bin`, or using it's relative file name:
			```shell
			[wilobyte@wilobyte-hp usr]$ pwd  
			/usr  
			[wilobyte@wilobyte-hp usr]$ cd ./bin  
			[wilobyte@wilobyte-hp bin]$ pwd  
			/usr/bin
			```
		- Note that in almost all cases, you can omit the `./` because it is implied. Typing `cd bin` does the same thing.
		- In general, if you do not specify a pathname, to something, the working directory will be assumed.
	- #### Filename Facts
		- Filenames that begin with a period character are hidden and can only be shown by using `ls -a`. These hidden files are mostly config files.
		- Filenames are case sensitive in Linux. *File1* and *file1* refer to different files.
		- Linux has no concept of a 'file extension', you can name them whatever you like. Although Unix-like operating systems do not use file extensions to determine the contents/purpose of files, some application programs do.
		- Though Linux supports long filenames that may contain embedded spaces and punctuations, limit the punctuations to period, dash (hyphen), and underscore. Most importantly, *do not embed spaces in filenames*. It will make command line tasks more difficult as we'll discover later. If you want to represent spaces between words in a filename, use the underscore.
---

## Commands / Code Snippets  
### Helpful `cd` shortcuts

| Shortcut       | Result                                                                                                                                                        |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `cd`           | Changes the working directory to your home directory                                                                                                          |
| `cd -`         | Changes the working directory to the previous working directory                                                                                               |
| `cd ~username` | Changes the working directory to the home directory of *username*. For example, `cd ~bond` changes the working directory to the home directory of user *bond* |

---

## System Behavior and Examples  
-  

---

## Practice Problems / Exercises  
-  Change to your home directory without using any pathnames

---

## Projects  


---

## Questions / Review Points  
-  Why does the Linux filesystem favour the root directory so much?
- What are the shortcuts used in relative pathnames?
- Why does Linux not have file extensions?

---

## Links to Related Notes  

---

## Tags  
#operatingsystems #{{topic}} #bash #to-review
