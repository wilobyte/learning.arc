# 01-06-IO_Redirection

**Date:** 2026-05-17  
**Subject:** Operating Systems and Systems Programming  
**Parent MOC:** [[TODO_LINK_THIS]]  
**Topic:** {{topic}}  
**Source / Reference:**  

---

## Learning Objectives  
-  Redirect input and output from multiple commands and connect them together to make pipelines
- A program mainly outputs *results* (**stdout**) and *status and error messages* (**stderr**)
- I/O redirection allows us to change where the output goes and where the input comes from. Usually, output goes to the screen and input from the keyboard
- ### Stdout Redirection
	- To store stdout of a command to a file, type the command followed by `>` (the redirect operator) followed by the name of the file. This purely stores stdout
	- `> file` makes an empty file since nothing is redirected to the file (nothing is currently in stdout)
	- `>> file` appends to the file rather than overwriting it
	- The redirect operators both create the file if it doesnt exist yet.
- ### Stderr Redirection
	- To redirect stderr, we need to use it's *file descriptor*, in addition with the redirect command.
	- Essentially, a program outputs on any of the available *file streams*, off which the first three being indexed as `0,1,2` are for stdin, stdout and stderr respectively.
	- So to redirect stderr error we use the notation of `cmd 2> file`
- If you want to redirect both stdout and stderr to a file, the following methods can be used:
	- `cmd > file 2>&1`, to explain this in this command whichever redirect is made first persists for the execution of this command only, first we redirected stdout to a file so anything further in this command being sent to stdout will automatically be sent to the file which is why the next part `2>&1` then pushes stderr to stdout which is now to the file before exiting. If the order was changed, `cmd 2>&1 > file`, this would first put stderr to the screen since the location of stdout has not been changed yet then after stderr has been moved to the screen, stdout is then moved to the file only.
	- Easier to use, `cmd &> file`
- Also if you do not want to display unwanted output like error or status messages from a program, you can redirect this to what's called a *bit bucket* which is `/dev/null`. `cmd 2> /dev/null`, basically `/dev/null` accepts input from a program and does nothing with it.
- ### Stdin Redirection
	- Here we will be looking primarily at the command `cat`, `cat` can be used to read files without paging and it can also merge multiple files for example, if we want to make a movie file out of frames we have we can simply use cat to read out these images then redirect them to one file, `cat > file1 file2...`. However, if not arguments are passed to `cat`, it reads directly from stdin, i.e the keyboard.
	- With the lack of file arguments it also copies stdin to stdout until the program is exited.
	- You can write to a file by simply using `cat > file`, typing whatever you want then exiting the program
	- `cat < file` redirects the contents of `file` to stdin, although the results are the same as passing a file name argument (it just reads whatever is contained within the file)
- ## Pipelines
	- The ability of commands to take standard input and send to standard output is done by  using the pipe operator `|`, by doing this the standard output of one command is *piped* as the standard input of the following command.
	- Usage: `command1 | command2`
	- For example we can pipe the output of `ls` into `less` to view it in the `less` pager. `ls <directory> | less`
	- ### Filters
		- Pipeline commands that take input manipulate it some way and send it to output are called *filers*. They can be chained together a lot in pipelines.
		- `sort` for example sorts whatever is passed to it in ordered manner. For example, if say, you want to list the contents of two directories, and view all of them as a sorted list, by default, `ls` would output the contents of the directories passed to it as two separate list, piping this output into `sort` however allows us to sort it into one singular list and then view or do whatever we want with it. So, `ls dir1 dir2 | sort | less`, sorts the contents of both directories into a single list and then is viewed in the less pager.
		- `uniq` removes duplicate lines in any sorted list of data passed to it either stdin or a single filename argument.
		- `wc`(word count), is used to display the number of lines, words and bytes contained in files.
		- `grep` is used to find text patterns within files, like this: `grep *pattern* [file...]`. When grep encounters a pattern in a file, it prints out the line(s) containing it.
		- `head`/`tail` only print the first and last 10 (by default) lines respectively of data passed to it or a file.
		- You can use `tail` to watch files in realtime (useful for stuff like log file) by using the `-f` (follow) option.
		- `tee` has the ability to copy standard input to both stdout and to a file. It can be useful when you want to see what's being done in the pipeline. For example, `ls /usr/bin | tee ls-output.txt | grep zip`, lists the contents of /usr/bin to stdout which is piped to`tee` which then copies bot to standout output *and* the file `ls-output.txt` before grepping it for zip.
- As always check out the `man` pages of the commands used in this note for more interesting insights.

---

## Concepts and Definitions  
-  

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
