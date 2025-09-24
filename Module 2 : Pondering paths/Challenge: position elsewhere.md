# Programs and absolute paths
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program which lies in a directory that we are not presently in and invoke program from there.
## My Solve
**Flag:** 'pwn.college{MbYBSSNqMn_x8ZTP0GAVbXFLLrR.QX3QTN0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. First you need to cd and go to the directory the program lies in.
```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /sys
hacker@paths~position-elsewhere:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{MbYBSSNqMn_x8ZTP0GAVbXFLLrR.QX3QTN0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program by providing its path on the command line even if the lie in a different directory from the one in use right now.
## References
None.
