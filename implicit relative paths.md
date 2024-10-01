# Implicit Relative paths

## Thought Process:
 upon encountering the problem, I was a bit confused on how to approach. After cross verifying a few sources, I first checked the directory I was currently in by 'pwd'. After that the same path was used as the previous questions
except over here no / was required since it was a relative path.

## Code:
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

## Learnings:
- A relative path doesnot begin with a '/'
- using the command pwd you can check your **present working directory**
- difference between an absolute path and relative path

## References
[https://www.youtube.com/watch?v=sB77xnFhsJs]<br>
[https://www.youtube.com/watch?v=AICr8jqgaEI]
