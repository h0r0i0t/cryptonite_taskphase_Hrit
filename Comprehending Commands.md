# Comprehending Commmands

## Challenge 1: cat: not the pet, but the command!

### Thought Process:
Quite a straightforward challenge. Passing cat command in home directory to access flag file.

### Code:
```bash
Connected!
pwn.college{0-L-O4WdwKQR9r6t22KE6557qho.dFzN1QDLyAjN0czW}
hacker@commands~cat-not-the-pet-but-the-command:~$ cat /flag
pwn.college{0-L-O4WdwKQR9r6t22KE6557qho.dFzN1QDLyAjN0czW}
```
### Learnings:
- Getting familiar with the cat command.

## Challenge 2: catting absolute path

### Thought Process:
Similar to the first challenge, all we do is use the cat command but this time use the absolute path for flag.

### Code:
```bash
Connected!
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{U6STeyhcaA2eGVxubr9W_YUu3ik.dlTM5QDLyAjN0czW}
```
### Learnings:
- Better understanding of using the cat function.

## Challenge 3: more catting practice

### Thought Process:
Despite not being able to cd, I simply used the absolute path provided to retrieve flag.

### Code:
```bash
Connected!
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /lib/tcltk/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /lib/tcltk/flag
pwn.college{8vBZzMOPHLm7Zk6rUZGDb2C_cKy.dBjM5QDLyAjN0czW}
```
### Learnings:
- Getting used to retrieve flag by cat using absolute paths.

## Challenge 4: grepping for a needle in a haystack

### Thought Process:
the first thing to do would be to cd to challenge directory. After doing so we use grep and use 'pwn.college' to locate our flag.

### Code:
```bash
Connected!
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ cd /challenge
hacker@commands~grepping-for-a-needle-in-a-haystack:/challenge$ grep pwn.college /challenge/data.txt
pwn.college{caE0N9mEhXxRguZo3-eOq9KzeqL.ddTM4QDLyAjN0czW}

```
### Learnings:
- Getting acquainted with the grep function.

  
## Challenge 5: listing files

### Code:
```bash
Connected!
hacker@commands~listing-files:~$ cd /challenge
hacker@commands~listing-files:/challenge$ ls
5534-renamed-run-21278  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ cat /challenge/5534-renamed-run-21278
#!/opt/pwn.college/bash
echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:/challenge$ /challenge/5534-renamed-run-21278
Yahaha, you found me! Here is your flag:
pwn.college{8a3gU0f3oNEi9FoDl-bOFV3c_un.dhjM4QDLyAjN0czW}
hacker@commands~listing-files:/challenge$

```
### Learnings:
- Understanding how the ls function works.


## Challenge 6: Touching files

### Thought Process:
I used cd to go tmp folder. Over there I used touch command to make the new files required.

### Code:
```bash
Connected!
Connected!
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ ls
bin  hsperfdata_root  tmp.MiOQGWw5Zc
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.MiOQGWw5Zc
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.MiOQGWw5Zc
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{8mUOnfjOIRP9HgJE3pTCv9UGiHg.dBzM4QDLyAjN0czW}
```
### Learnings:
- The use of touch command to create new files.

## Challenge 7: removing files

### Thought Process:
I used the ls command in home directory to see the file to be deleted. Then it was all a matter of running the rm command.

### Code:
```bash
Connected!
hacker@commands~removing-files:~$ ls
delete_me  t
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{EC0u_xkX57sPBSDZyH9ooe_iulK.dZTOwUDLyAjN0czW}
```
### Learnings:
- Getting familiar with the rm command.

## Challenge 8: hidden files

### Thought Process:
First I cd to / directory after which using the ls with -a, i found the hidden file. Lastly by using cat funtion i  read the file and got the flag.

### Code:
```bash
Connected!
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-284723086713151  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-284723086713151
pwn.college{ImBzkxagiPCM5hl7syf3he2mdtY.dBTN4QDLyAjN0czW}
```
### Learnings:
- Hidden files begin with a '.'
- ls function typically doesnot display it when invoked.
- we must execute ls -a to see these hidden files



## Challenge 9: An Epic Filesystem Quest:

### Thought Process:
First I cd to / directory after which using the ls with -a, i found the hidden file. Lastly by using cat funtion i  read the file and got the flag.

### Code:
```bash
Connected!
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-284723086713151  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-284723086713151
pwn.college{ImBzkxagiPCM5hl7syf3he2mdtY.dBTN4QDLyAjN0czW}
```
### Learnings:
- Hidden files begin with a '.'
- ls function typically doesnot display it when invoked.
- we must execute ls -a to see these hidden files.

