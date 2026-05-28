# 01-03-File_And_Directory_Structure

**Date:** 2025-08-15  
**Subject:** Operating Systems and Systems Programming  
**Parent MOC:** [[01_Command_Line_Basics_MOC]]  
**Topic:** {{topic}}  
**Source / Reference:**  [The linux command line, shotts](obsidian://open?vault=learning.arc&file=04_Operating_Systems_and_Systems_Programming%2F01_Bash_and_Linux%2F01_Resources%2F01_The_Linux_Command_Line_Shotts.pdf)

---

## Learning Objectives  
-  Move around and investigate the filesystem.
- Learn the commands:
	- `ls` - List directory contents.
	- `file` - Determine file type.
	- `less` - View file contents.

---

## Concepts and Definitions  
- ### The `ls` Command 
	- We can use this command to see the directory contents and determine some important file and directory attributes.
	- As we have seen earlier, the `ls` command will list whatever files or subdirectories are in the current working directory when passed to the shell.
	- Besides the current working directory, we can specify the directory to list, like so:
		```bash
		[wilobyte@wilobyte-hp ~]$ ls /usr  
		bin  include  lib  lib32  lib64  local  sbin  share  src
		```
	- You can even specify multiple directories, for example to list the home directory and the */usr* directory, we can use the following command:
		```bash
		[wilobyte@wilobyte-hp ~]$ ls ~ /usr
		/home/wilobyte:  
		basic.py   Documents   Music      Public   tagainijisho   Videos  
		Desktop    Downloads   Pictures   python   Templates     'VirtualBox VMs'  
		  
		/usr:  
		bin  include  lib  lib32  lib64  local  sbin  share  src
		```
	- We can also change the format of the output to reveal more detail:
		```bash
		[wilobyte@wilobyte-hp ~]$ ls -l  
		total 48  
		-rw-r--r-- 1 wilobyte wilobyte   46 Aug 11 10:22  basic.py  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Desktop  
		drwxr-xr-x 6 wilobyte wilobyte 4096 Jul 23 14:11  Documents  
		drwxr-xr-x 6 wilobyte wilobyte 4096 Aug 13 06:22  Downloads  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  8 09:14  Music  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 29 05:13  Pictures  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Public  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  9 06:01  python  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 23 01:28  tagainijisho  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Templates  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 29 05:13  Videos  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 24 15:39 'VirtualBox VMs'
		```
	- By adding the `-l` option, we changed the input to the *long format*.
- ### Options and Arguments
	- Commands are usually followed by one or more *options* which modify how the command works followed by one or more *arguments*, the items which the command acts on.
	- So, most commands have the following structures:
		```bash
		command -options arguments
		```
	- Most commands use options consisting of a single character preceded like a dash, such as `-l`. Many commands allow multiple short options to be strung together too.
	- Many commands, including the ones from the GNU Project, use *long options* which are preceded by two dashes.
	- In the example below, we string two short options; `l` to produce the long format output, and the `t` option to sort them by the file's modification time.
		```bash
		[wilobyte@wilobyte-hp ~]$ ls -lt  
		total 48  
		drwxr-xr-x 6 wilobyte wilobyte 4096 Aug 13 06:22  Downloads  
		-rw-r--r-- 1 wilobyte wilobyte   46 Aug 11 10:22  basic.py  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 29 05:13  Videos  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 29 05:13  Pictures  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 24 15:39 'VirtualBox VMs'  
		drwxr-xr-x 6 wilobyte wilobyte 4096 Jul 23 14:11  Documents  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 23 01:28  tagainijisho  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  9 06:01  python  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  8 09:14  Music  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Desktop  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Public  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Templates
		```
	- We can add the long option `--reverse` to reverse the order of the text.
		```bash
		[wilobyte@wilobyte-hp ~]$ ls -lt --reverse
		total 48  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Templates  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Public  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35  Desktop  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  8 09:14  Music  
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  9 06:01  python  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 23 01:28  tagainijisho  
		drwxr-xr-x 6 wilobyte wilobyte 4096 Jul 23 14:11  Documents  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 24 15:39 'VirtualBox VMs'  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 29 05:13  Pictures  
		drwxr-xr-x 3 wilobyte wilobyte 4096 Jul 29 05:13  Videos  
		-rw-r--r-- 1 wilobyte wilobyte   46 Aug 11 10:22  basic.py  
		drwxr-xr-x 6 wilobyte wilobyte 4096 Aug 13 06:22  Downloads
		```
	- The `ls` command has a large number of possible options. Here's a few useful ones:
		
		| Option | Long Option        | Description                                                                                                                                                                                                                                 |
		| ------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
		| `-a`   | `--all`            | List all files, including those that start with a period character which are usually hidden                                                                                                                                                 |
		| `-d`   | `--directory`      | Lists the directories themselves and not their contents. Normally when you pass a directory pathname argument to the `ls` command it prints it's contents. String this option with the `-l` option to show information about the directory. |
		| `-F`   | `--classify`       | Appends an indicator character to the end of each listed name. (for example, a forward slash if the name is a directory).                                                                                                                   |
		| `-h`   | `--human-readable` | In long format listings, display file sizes in human-readable format (like 1k, 224M, 2G) rather than in bytes.                                                                                                                              |
		| `-l`   |                    | Displays results in long format.                                                                                                                                                                                                            |
		| `-r`   | `--reverse`        | Displays the results in reverse order. Normally, `ls` displays the results in alphabetical order.                                                                                                                                           |
		| `-s`   |                    | Sorts results by file size.                                                                                                                                                                                                                 |
		| `-t`   |                    | Sorts results by modification time.                                                                                                                                                                                                         |
- ### The Long Format
	- As we've seen, the `-l` option causes `ls` to display it's results in long format.
	- The long format contains a lot of useful information.
	- Here's an example of the long format:
		```bash
		[wilobyte@wilobyte-hp ~]$ ls -ld Desktop/    
		drwxr-xr-x 2 wilobyte wilobyte 4096 Jul  7 00:35 Desktop/
		```
	- Here's the breakdown of the fields of the long format as well as what they mean:
		
		| Field          | Meaning                                                                                                                                                                                                                                                                                                                                                                      |
		| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
		| `drwxr-xr-x`   | Access rights to the file. The first character indicates the type of file. A leading dash represents a regular file, while a `d` indicates a directory. The nest 3 characters are the access rights for the files owner, the next three are for members of the file group and the final three are for everyone else. We'll take a look at what this all means going forward. |
		| `2`            | File's number of hard links.                                                                                                                                                                                                                                                                                                                                                 |
		| `wilobyte`     | The user name of the file's owner.                                                                                                                                                                                                                                                                                                                                           |
		| `wilobyte`     | The name of the group that owns the file.                                                                                                                                                                                                                                                                                                                                    |
		| `4096`         | Size of the file in bytes.                                                                                                                                                                                                                                                                                                                                                   |
		| `Jul  7 00:35` | Date and time of the file's last modification.                                                                                                                                                                                                                                                                                                                               |
		| `Desktop/`     | Name of the file.                                                                                                                                                                                                                                                                                                                                                            |
- ### Determining a File's Type with `file`
	- Filenames in Linux don't necessarily have to reflect what the file contains. 
	- For example, we would normaly expect the filename *picture.jpeg* to be a JPEG compressed image, it is not required to be so however in Linux.
	- We use the `file` command to determine the file's type as shown below:
		```bash
		file *filename*
		```
	- When invoked, the `file` command will print a brief description of the file's contents:
		```bash
		[wilobyte@wilobyte-hp Downloads]$ file picture.jpeg  
		picture.jpeg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x7  
		2, segment length 16, Exif Standard: [TIFF image data, big-endian, direntries=5,  
		orientation=upper-left, xresolution=74, yresolution=82, resolutionunit=2], progre  
		ssive, precision 8, 736x1308, components 3
		```
- ### Viewing File Contents with `less`
	- The `less` command is a program used to view text files.
	- There are many files in Linux that contain human-readable text, and the `less` command gives us a convenient way to examine them.
	- Many text files contain system settings (called *config files*) are stored in this format and being able to inspect them will give insights into how the system works.
	- Many of the actual programs the system uses (called *scripts*) are stored in this format as well.
	- The `less` command is used as so:
		```bash
		less *filename*
		```
	- Once started, the `less` program allows you to scroll backwards and forwards through a text file.
	- Here's some common keyboard commands used by `less`:
		
		
		| Command                   | Action                                               |
		| ------------------------- | ---------------------------------------------------- |
		| `PAGE UP` or `b`          | Scroll back one page                                 |
		| `PAGE DOWN` or `Spacebar` | Scroll forward one page                              |
		| `Up Arrow`                | Scroll up one line                                   |
		| `Down Arrow`              | Scroll down one lline                                |
		| `G`                       | Move to the end of the text file                     |
		| `1G` or `g`               | Move to the beginning of the text file               |
		| `/characters`             | Search forward to the next occurence of *characters* |
		| `n`                       | Search for the next occurence of the previous search |
		| `h`                       | Display help screen                                  |
		| `q`                       | Quit less                                            |
	- The `less` program was made as a replacement for an old program `more`. *less is more* (get it?). `less` is an example of a *pager* program which views text documents in a page-by-page manner. Whereas the `more` program can only page forward, the `less` program can page backwards and forwards and has loads of other features as well.


---

## Commands / Code Snippets  

``` insert commands or scripts here
```
---

## System Behavior and Examples  
-  

---

## Practice Problems / Exercises  
-  

---

## Projects  
- Related project(s):  
  - [Project Name](./Projects/Project_Name/)  

---

## Questions / Review Points  
-  

---

## Links to Related Notes  

---

## Tags  
#operatingsystems #{{topic}} #bash #to-review
