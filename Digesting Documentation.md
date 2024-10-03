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

## Challenge 2: Learning Complex Usage

### Thought Process:
The analogy if the -name argument that we pass with find helped me understand what to do. Basically we have to pass another argument for a given argument. By this logic, I managed to solve this challenge.

### Code: 
```bash
Connected!
hacker@man~learning-complex-usage:~$ cd /
hacker@man~learning-complex-usage:/$ cd /challenge
hacker@man~learning-complex-usage:/challenge$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](../commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!.
hacker@man~learning-complex-usage:/challenge$ ls
DESCRIPTION.md  challenge
hacker@man~learning-complex-usage:/challenge$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{c_yEMt-7lViHTkD34UvnPLAOQPh.dVjM5QDLyAjN0czW}
```
### Learnings:
- Understanding how arguments can also have arguments for themselves.
- More clarity with what we did during the 'finding files' module challenge.
- 
