# Path Pondering


## The Root


### Code:
```bash
Connected!
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{kqFWnscuczX2Jdl1qnkKD_9Itok.dhzN5QDLyAjN0czW}
hacker@paths~the-root:~$
```
### Learnings:
-File Systems start with a '/' <br>
-an **Absolute Path** refers to a path which starts from a root directory. 

## Program and Absolute paths
### Code:
```bash
Connected!
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{gJSxbN1_G51xU6MuE-Dd2mrGSSa.dVDN1QDLyAjN0czW}

```
### Learnings:
- To invoke the absolute path of a file


## Position thyself
### Code:
```bash
hacker@paths~position-thy-self:/$ cd /
hacker@paths~position-thy-self:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@paths~position-thy-self:/$ cd /challenge
hacker@paths~position-thy-self:/challenge$ /challenge/run
Incorrect...
You are not currently in the /proc/84 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:/challenge$ cd /proc/84
hacker@paths~position-thy-self:/proc/84$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gVjH-TyLavXlF8ghfJTvogU9ZVo.dZDN1QDLyAjN0czW}
hacker@paths~position-thy-self:/proc/84$
```
### Learnings:

- how to use cd command to navigate through directories 
- '`' refers to the current that my shell is at 

### References:
- [https://www.youtube.com/watch?v=TPF-eIe-ucU]
- [https://opensource.com/resources/what-bash]

## Position elsewhere
### Code:
```bash
Connected!
hacker@paths~position-elsewhere:~$ cd /
hacker@paths~position-elsewhere:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@paths~position-elsewhere:/$ cd /challenge
hacker@paths~position-elsewhere:/challenge$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/challenge$ cd /
hacker@paths~position-elsewhere:/$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{oYYYDO0cUP8JEeNeY9VCLZjmEI0.ddDN1QDLyAjN0czW}
```
### Learnings:
- Better understanding on how we cd to a directory and run a text.

## Position yet elsewhere.

### Thought Process:
As the previous two solves have taught, the approach to be taken is to attempt to run the command on a certain directory. If incorrect, it displays the required directory.

### Code:
```bash
hacker@paths~position-yet-elsewhere:/bin$ cd /
hacker@paths~position-yet-elsewhere:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@paths~position-yet-elsewhere:/$ cd /challenge
hacker@paths~position-yet-elsewhere:/challenge$ /challenge/run
Incorrect...
You are not currently in the /sys/kernel directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:/challenge$ cd /sys/kernel
hacker@paths~position-yet-elsewhere:/sys/kernel$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{sUww0qAnWrzlFOq9wlhn1KP8vqS.dhDN1QDLyAjN0czW}
hacker@paths~position-yet-elsewhere:/sys/kernel$
```


in which we must run the given command. In this case it was /sys/kernel.
### Learnings:
-further developing understanding on changing directories.



## Implicit Relative paths

### Thought Process:
 upon encountering the problem, I was a bit confused on how to approach. After cross verifying a few sources, I first checked the directory I was currently in by 'pwd'. After that the same path was used as the previous questions
except over here no / was required since it was a relative path.

### Code:
```bash
hacker@paths~implicit-relative-paths-from-:/$ cd /
hacker@paths~implicit-relative-paths-from-:/$ pwd
/
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Y23C9JEAycOGGds7xNH4bo4URUs.dlDN1QDLyAjN0czW}
```

### Learnings:
- A relative path doesnot begin with a '/'
- using the command pwd you can check your **present working directory**
- difference between an absolute path and relative path

## Explicit relative paths

### Thought Process
With the help of the provided example, I was able to invoke the path with ease.
  
### Code:
```bash
Connected!
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IZLLg3eSmEG7P5ua_TFSY2DJDHb.dBTN1QDLyAjN0czW}
```
### Learnings:
- '.' is an implicit entry the refers to the same directory
  

### References
[https://www.youtube.com/watch?v=sB77xnFhsJs]<br>
[https://www.youtube.com/watch?v=AICr8jqgaEI]

## implicit Relative Path

### Thought Process
Similar to the previous module, using the . operator we explicitly tell Linux to run the relative path and execute the program

### Code
```bash
Connected!
hacker@paths~implicit-relative-path:~$ cd /
hacker@paths~implicit-relative-path:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@paths~implicit-relative-path:/$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{wSCOToxgwQNtzSsfuu1LBYBlM2J.dFTN1QDLyAjN0czW}
```

### Learnings:
- better understanding of the '.' operator to execute relative paths



## Home Sweet Home

### Thought Process:
This was a bit confusing when first read. I tried a few older methods used but to no avail. However after reading the example given I was able to figure out the syntax 
to be passed. The last 3 line gave big hints:
1) Argument must be an absolute path so it must begin with a '/' 
2) Since we must do it in home directory, there is no need to go into any file
3) It must be 3 letters hence we can ~/x  where x is anything of my choice

### Code:
```bash
hacker@paths~home-sweet-home:~$ cd /
hacker@paths~home-sweet-home:/$ /challenge/run ~/abc
The argument you provided must not have been longer than 3 characters (it's
currently 5 characters long)!
hacker@paths~home-sweet-home:/$ /challenge/run ~/t
Writing the file to /home/hacker/t!
... and reading it back to you:
pwn.college{gA3i01EW6IhqOBheuhb5CBakCHT.dNzM4QDLyAjN0czW}
```

### Learnings:
- A better understanding on the use of the '~' function
- ~ is a shorthand for your home directory

