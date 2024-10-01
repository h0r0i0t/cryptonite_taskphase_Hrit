# implicit Relative Path

## Thought Process
Similar to the previous module, using the . operator we explicitly tell Linux to run the relative path and execute the program

## Code
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

## Learnings:
- better understanding of the '.' operator to execute relative paths
