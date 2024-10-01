# Home Sweet Home

## Thought Process:
This was a bit confusing when first read. I tried a few older methods used but to no avail. However after reading the example given I was able to figure out the syntax 
to be passed. The last 3 line gave big hints:
1) Argument must be an absolute path so it must begin with a '/' 
2) Since we must do it in home directory, there is no need to go into any file
3) It must be 3 letters hence we can ~/x  where x is anything of my choice

## Code:
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

## Learnings:
- A better understanding on the use of the '~' function
- ~ is a shorthand for your home directory
  
