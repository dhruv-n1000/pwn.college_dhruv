# The Root
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the program by providing its path on the command line.

## My Solve
**Flag:** 'pwn.college{4jwMLDlIf0Sr5Xx7F2mnG2zYYvz.QX4cTO0wSOxkjNzEzW}'

A program can be invoked by supplying its path on the command line. Here, you will provide the full path starting with /, which is /pwn. This type of path, which begins with the root directory, is called an "absolute path."
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{4jwMLDlIf0Sr5Xx7F2mnG2zYYvz.QX4cTO0wSOxkjNzEzW}
```

## What I Learned
I learnt how Linux commands can be used to invoke a program by providing its path on the command line, we have to give the exact path starting from /, so the path would be /pwn.
## References
None.
