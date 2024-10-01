# Position yet elsewhere.

## Code:
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

## Thought Process:
As the previous two solves have taught, the approach to be taken is to attempt to run the command on a certain directory. If incorrect, it displays the required directory
in which we must run the given command. In this case it was /sys/kernel.
## Learnings:
-further developing understanding on changing directories
