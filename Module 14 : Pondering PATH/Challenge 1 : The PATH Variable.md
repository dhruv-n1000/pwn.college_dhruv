## The PATH Variable
This challenge requires us to change the value of PATH variable.

### Solve
**Flag:** 'pwn.college{wazUUUADR0u4g-Luc7Tr5F6IU3E.QX2cDM1wSOxkjNzEzW}'


We simply had to change the value of the variable PATH="" so that the program cannot find the PATH to the 'rm' command which was supposed to remove the flag on execution
of /challenge/run.
```
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{wazUUUADR0u4g-Luc7Tr5F6IU3E.QX2cDM1wSOxkjNzEzW}

```

### What I Learnt
I learnt that if we change the PATH of a command, it can stop the program from getting its location and hence render the command useless.
### References 
None.
