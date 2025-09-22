# Programs and absolute paths
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program in a directory which is furthur in a directory by providing its path on the command line

## My Solve
**Flag:** 'pwn.college{AEtoSiRcKoJcwea8DjMtxo_jmTK.QX1QTN0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. Here, you will provide the full path starting with /challenge and then /run so net path is /challenge/run. This type of path, which begins with the root directory, is called an "absolute path."
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{AEtoSiRcKoJcwea8DjMtxo_jmTK.QX1QTN0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program by providing its path on the command line, we have to give the exact path starting from /, so the path would be /challenge/run.
## References
None.
