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
It was quite a long find. Wherever I got stuck I simply referred to the previous modules for help, as we have already done these functions indivisualy in them. After a point it became easy as we were simply repeating the same steps.

### Code:
```bash
hrit0306@LAPTOP-5JBTL6AI:~$ ssh -i ./key hacker@dojo.pwn.college
Connected!
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
LEAD  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin   challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat LEAD
Tubular find!
The next clue is in: /opt/linux/linux-5.4/arch/powerpc/platforms/85xx

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ /opt/linux/linux-5.4/arch/powerpc/platforms/85xx
ssh-entrypoint: /opt/linux/linux-5.4/arch/powerpc/platforms/85xx: Is a directory
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/arch/powerpc/platforms/85xx
INFO-TRAPPED   common.c           mpc85xx_ads.c     mvme2500.c   qemu_e500.c    socrates_fpga_pic.c  xes_mpc85xx.c
Kconfig        corenet_generic.c  mpc85xx_cds.c     p1010rdb.c   sbc8548.c      socrates_fpga_pic.h
Makefile       ge_imp3a.c         mpc85xx_ds.c      p1022_ds.c   sgy_cts1000.c  stx_gp3.c
bsc913x_qds.c  ksi8560.c          mpc85xx_mds.c     p1022_rdk.c  smp.c          t1042rdb_diu.c
bsc913x_rdb.c  mpc8536_ds.c       mpc85xx_pm_ops.c  p1023_rdb.c  smp.h          tqm85xx.c
c293pcie.c     mpc85xx.h          mpc85xx_rdb.c     ppa8548.c    socrates.c     twr_p102x.c
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/arch/powerpc/platforms/85xx/INFO-TRAPPED
Great sleuthing!
The next clue is in: /usr/share/racket/pkgs/readline-lib/readline

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/racket/pkgs/readline-lib/readline
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/readline-lib/readline$ ls
EVIDENCE  compiled  main.rkt  pread.rkt  readline.rkt  rep-start.rkt  rep.rkt  rktrl.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/readline-lib/readline$ cat EVIDENCE
Tubular find!
The next clue is in: /usr/share/doc/python3-docutils
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/readline-lib/readline$ cd /usr/share/doc/python3-docutils
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-docutils$ ls
BUGS.txt.gz  HISTORY.txt.gz  README.txt.gz         SPOILER     changelog.Debian.gz  copyright
FAQ.txt.gz   NEWS.Debian.gz  RELEASE-NOTES.txt.gz  THANKS.txt  changelog.gz
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-docutils$ cat SPOILER
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/nbclient-0.10.0.dist-info

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-docutils$ cd /usr/local/lib/python3.8/dist-packages/nbclient-0.10.0.dist-info
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/nbclient-0.10.0.dist-info$ ls -a
.  ..  .SECRET  INSTALLER  METADATA  RECORD  WHEEL  entry_points.txt  licenses
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/nbclient-0.10.0.dist-info$ cat .SECRET
Great sleuthing!
The next clue is in: /opt/ghidra/docs/GhidraClass/Advanced/Examples

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/nbclient-0.10.0.dist-info$ cd /opt/ghidra/docs/GhidraClass/Advanced/Examples
hacker@commands~an-epic-filesystem-quest:/opt/ghidra/docs/GhidraClass/Advanced/Examples$ ls -a
.   .README   animals.cpp             createStructure.c  dataMutability.c  inline.s                 ldiv.c      opaque.c    setRegister.c   switch.s
..  Makefile  compilerVsDecompiler.s  custom.c           globalRegVars.c   jumpWithinInstruction.c  noReturn.c  override.c  sharedReturn.c  write.c
hacker@commands~an-epic-filesystem-quest:/opt/ghidra/docs/GhidraClass/Advanced/Examples$ CAT .README
ssh-entrypoint: CAT: command not found
hacker@commands~an-epic-filesystem-quest:/opt/ghidra/docs/GhidraClass/Advanced/Examples$ cat .README
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/amd/include/asic_reg/gc
hacker@commands~an-epic-filesystem-quest:/opt/ghidra/docs/GhidraClass/Advanced/Examples$ cd /opt/linux/linux-5.4/drivers/gpu/drm/amd/include/asic_reg/gc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/include/asic_reg/gc$ ls
HINT                 gc_10_1_0_offset.h   gc_9_0_default.h  gc_9_0_sh_mask.h  gc_9_1_sh_mask.h   gc_9_2_1_sh_mask.h
gc_10_1_0_default.h  gc_10_1_0_sh_mask.h  gc_9_0_offset.h   gc_9_1_offset.h   gc_9_2_1_offset.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/include/asic_reg/gc$ cat HINT
Great sleuthing!
The next clue is in: /opt/aflplusplus/qemu_mode/qemuafl/tests/tcg/ppc

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/amd/include/asic_reg/gc$ cd /opt/aflplusplus/qemu_mode/qemuafl/tests/tcg/ppc
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/qemu_mode/qemuafl/tests/tcg/ppc$ ls
DISPATCH  Makefile.target
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/qemu_mode/qemuafl/tests/tcg/ppc$ cat DISPATCH
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/include/config/sparsemem

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/aflplusplus/qemu_mode/qemuafl/tests/tcg/ppc$ cd /opt/linux/linux-5.4/include/config/sparsemem
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/sparsemem$ ls
NUGGET  extreme.h  manual.h  vmemmap  vmemmap.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/sparsemem$ cat NUGGET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{MyBCaXht4C23dNi1oTFlq9ZnUuG.dljM4QDLyAjN0czW}
```
### Learnings:
- Proper understanding of how to use cat
- Better understanding on how to absolute paths and how to refer to directories without cd'ing into them
- Revision of syntax of previous functions

