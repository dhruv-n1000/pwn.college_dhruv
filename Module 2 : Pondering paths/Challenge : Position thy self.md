# Position thy self
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program in a specific directory which is not initially in use, but we have to change the directory to get to that directory.
## My Solve
**Flag:** 'pwn.college{gg5T7BwZajOdlwhPDMnCMBqQC3h.QX2QTN0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. Here, we have to initially change the default directory to the directory they give us after initial running, after changing the directory, we just invoke the absolute path of the program.
```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /proc/203/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /proc/203/fd
hacker@paths~position-thy-self:/proc/203/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gg5T7BwZajOdlwhPDMnCMBqQC3h.QX2QTN0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program in a different directory by providing its path on the command line after changing the directory using cd initially, we have to give the exact path starting from /, so the path would be /challenge/run.
## References
None.
