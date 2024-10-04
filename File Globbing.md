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


  ## Challenge 3: Matching with []

  ### Thought Process
  Similar to the previous two challenges, using the [] character I accessed the files needed and ran /challenge/run to get the flag

### Code:
```bash
Connected!
hacker@globbing~matching-with-:~$ cd /
hacker@globbing~matching-with-:/$ /challenge/files
ssh-entrypoint: /challenge/files: Is a directory
hacker@globbing~matching-with-:/$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{Av1oLz0zPMDjRS7o_q3zcQowFmC.dNjM4QDLyAjN0czW}
```

### Learnings:
- How to use the [] character to match potential characters that fit a certain description.


## Challenge 4: Matching with []

  ### Thought Process
  Similar to the previous two challenges, using the [] character I accessed the files needed and ran /challenge/run to get the flag

### Code:
```bash
Connected!
hacker@globbing~matching-with-:~$ cd /
hacker@globbing~matching-with-:/$ /challenge/files
ssh-entrypoint: /challenge/files: Is a directory
hacker@globbing~matching-with-:/$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{Av1oLz0zPMDjRS7o_q3zcQowFmC.dNjM4QDLyAjN0czW}
```

### Learnings:
- How to use the [] character to match potential characters that fit a certain description.
