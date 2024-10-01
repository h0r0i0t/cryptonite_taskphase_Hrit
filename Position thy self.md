# Position thyself
## Code:
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
## Learnings:

- how to use cd command to navigate through directories 
- '`' refers to the current that my shell is at 

## References:
- [https://www.youtube.com/watch?v=TPF-eIe-ucU]
- [https://opensource.com/resources/what-bash]
