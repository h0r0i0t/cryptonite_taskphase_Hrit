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

## Challenge 3: Reading Manuels

### Thought Process:
After using man I was displayed a few arguments that I could use. Initially while I was confused, I tried using all arguments. The last one had a num value to it. First I tried using it ith just 'NUM' but got an error. After reading the text after that, which said to print it using the number 269. It worked.

### Code:
```bash
Connected!
hacker@man~reading-manuals:~$ cd /
hacker@man~reading-manuals:/$ man challenge

CHALLENGE(1)                                                       Challenge Commands                                                       CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --cweqjb NUM
              print the flag if NUM is 269

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                                             May 2024                                                            CHALLENGE(1)
hacker@man~reading-manuals:/$ /challenge/challenge
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:/$ /challenge/challenge --fortune
Even if you do learn to speak correct English, whom are you going to speak
it to?
                -- Clarence Darrow
hacker@man~reading-manuals:/$ /challenge/challenge --version
I'm exactly the version I need to be!
hacker@man~reading-manuals:/$ /challenge/challenge cweqjb  NUM
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:/$ /challenge/challenge --cweqjb NUM
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:/$ /challenge/challenge --cweqjb 269
Correct usage! Your flag: pwn.college{ILc2P6we97q2Mjb5KUCllUky6xu.dRTM4QDLyAjN0czW}
```

### Learnings: 
- Understanding how to use the man command.
- we can use 'q' to quit the manuel when required.
- we dont need to use file paths to invoke the man command, only the entry will do.

## Challenge 4: Searching Manuels

### Thought Process
Using the man command many arguements were displayed for /challenge/challenge. By using ./flag, I found the argument which would give me the flag

### Code:
```bash
Connected!
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ajzuu
Initializing...
Correct usage! Your flag: pwn.college{I43dh9OEHJHvQ0sUd1V5fm25HDP.dVTM4QDLyAjN0czW}
```
### Learnings:
- Introduction to the man command

### References:
[https://www.youtube.com/watch?v=-CTBgNO-MHY]

## Challenge 6: Helpful Programs

### Thought Process
Running the --help command on /challenge/challenge, we get some information. one of which says that we can get the flag by running some value with -g, and another one which says that you can get the number by -p. Simply running these commands gives us these answers.

### Code:
```bash
Connected!
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 334
hacker@man~helpful-programs:~$ /challenge/challenge -g 334
Correct usage! Your flag: pwn.college{IrLLy3xUx-dUE3FrQeBS4QSLqz9.ddjM4QDLyAjN0czW}
```
### Learnings:
- how to use the --help command when we cant use man to get some more information on a certain program that doesnot hacve a designated manpage for it.


## Challenge 7: Help for Buildins

### Thought Process
simply by using the help command, we get all the information we need to get the flag. A secret value is given and the argument needed to pass to the value.

### Code:
```bash
Connected!
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AouoMN64".
hacker@man~help-for-builtins:~$ challenge --fortune
The public demands certainties;  it must be told definitely and a bit
raucously that this is true and that is false.  But there are no certainties.
                -- H. L. Mencken, "Prejudice"
hacker@man~help-for-builtins:~$ challenge --version
I'm exactly the version I need to be!
hacker@man~help-for-builtins:~$ challenge --secret AouoMN64
Correct! Here is your flag!
pwn.college{AouoMN64mdCyP3_lwN2Y6_duZHs.dRTM5QDLyAjN0czW}
```
### Learnings:
- How to acess buildin commands and their use.


