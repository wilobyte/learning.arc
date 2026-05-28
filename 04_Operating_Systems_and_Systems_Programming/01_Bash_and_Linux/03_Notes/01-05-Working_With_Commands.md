# 01-05-Working_With_Commands

**Date:** 2026-02-07  
**Subject:** Operating Systems and Systems Programming  
**Parent MOC:** [[TODO_LINK_THIS]]  
**Topic:** {{topic}}  
**Source / Reference:**  

---

## Learning Objectives  
-  `type which man apropos info whatis alias` 

---

## Concepts and Definitions  
-  Command can be one of four things:
	- An executable such as the ones in usr/bin sometimes compiled binaries (c and cpp) and other written in scripting languages (shell, Python etc)
	- Shell builtins are commands that come with the shell by default for example `cd`
	- Shell functions - miniature shell scripts incorporated into the environment (to be treated later)
	- Alias - these are commands we define by ourselves, built from other commands.
- Now sometimes, we may need to know what type of command we're using and we have a bunch of tools which we'll look at for accomplishing this:
	- The `type` command is used to display a command's type. It's syntax is the following: `type command` which displays the type of command, most commonly it shows whether the argument in the command is a shell builtin, an alias or an executable. (For examples, take a look at the code snippets below).
	- The `which` command displays an executable's location. This can be useful because we might have two versions of a program installed. This command only works with executables and not shell builtins or aliases; it will throw up an error if those are passed.
- We can also take a look at documentation for various commands

---

## Commands / Code Snippets  

```shell
wilobyte@keisanki:~$ type cd
cd is a shell builtin
wilobyte@keisanki:~$ type cp
cp is /usr/bin/cp
wilobyte@keisanki:~$ type anki
anki is /usr/local/bin/anki
wilobyte@keisanki:~$ type start-shizuku
start-shizuku is aliased to `adb shell sh /storage/emulated/0/Android/data/moe.shizuku.privileged.api/start.sh'
wilobyte@keisanki:~$ 
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
