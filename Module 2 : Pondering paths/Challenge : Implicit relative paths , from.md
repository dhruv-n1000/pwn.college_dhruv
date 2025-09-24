# Implicit relative paths , from /
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program using the path relative to the current working directory.
## My Solve
**Flag:** 'pwn.college{sxeg5hwKVejWphe4-7SsLXahrzu.QX5QTN0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. First you need to cd and go to the directory the program lies in.
```
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sxeg5hwKVejWphe4-7SsLXahrzu.QX5QTN0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program by providing its relative path on the command line with respect to the current working directory.
## References
None.
