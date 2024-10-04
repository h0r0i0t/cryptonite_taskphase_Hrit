# File Globbing: 

## Challenge 1: Matching with *

### Thought Process
Quite a straightforward question. Using the * function I cd to challenge and ran the command

### Code:
```bash
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{4TcyRB8s4F3rThVAN8Q9gsHC_qJ.dFjM4QDLyAjN0czW}
```
### Learnings:
- How to use the '*' character to find files.


## Challenge 2: Matching with ?

### Thought Process
Similar to the previous challenge, using the ? character instead of the c and l alphabet I found the file required

### Code:
```bash
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{APl7SB_3aF6_mTq8hfiXy7PeZgi.dJjM4QDLyAjN0czW}
```
### Learnings:
- How to use the '?' character is used to find files
