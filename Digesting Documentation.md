# Digesting Documentation
## Challenge 1: Learning From Documentation

### Thought Process: 
Since we have already learnt how to get hidden files through -a and forming links by -s, the following question operates on the same logic. It is teaching us how to pass arguments. This question is quite straightforward. There were a few errors
made by me when it came to formatting but I managed to get the flag.

### Code:
```bash
hacker@man~learning-from-documentation:~$ cd /
hacker@man~learning-from-documentation:/$ cd /challenge
hacker@man~learning-from-documentation:/challenge$ ls
DESCRIPTION.md  challenge
hacker@man~learning-from-documentation:/challenge$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{M9uYjgo78L8C8l13DAD5mgMRkmv.dRjM5QDLyAjN0czW}
```

### Learnings:
- Understanding documentation and how to mass arguments

