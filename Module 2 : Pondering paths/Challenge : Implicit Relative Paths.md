# Implicit relative path
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program using the path relative to the current working directory.
## My Solve
**Flag:** 'pwn.college{gZV2-SizAgZjV_QxrEdRSWgrUfv.QXxUTN0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. First you need to cd and go to the directory the program lies in.
```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gZV2-SizAgZjV_QxrEdRSWgrUfv.QXxUTN0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program by providing its relative path on the command line with respect to the current working directory.
## References
None.
