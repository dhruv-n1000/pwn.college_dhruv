# Explicit Relative Paths, from /
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program using the path relative to the current working directory, using '.' .
## My Solve
**Flag:** 'pwn.college{0mYilG06DVb2jbA--nkchQthMVA.QXwUTN0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. First you need to use 'cd' and go to the '/' directory, then using relative path and '.' go the program you want to invoke.
```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0mYilG06DVb2jbA--nkchQthMVA.QXwUTN0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program by providing its relative path on the command line with respect to the current working directory using '.' .
## References
None.
