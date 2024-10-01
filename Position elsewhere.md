# Position elsewhere
## Code:
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
## Learnings:
- Better understanding on how we cd to a directory and run a text
