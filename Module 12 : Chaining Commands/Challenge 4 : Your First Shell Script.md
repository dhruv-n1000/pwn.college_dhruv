## Your First Shell Script
This challenge requires us to create a shell script and use it to run the lines of program stored in it to save space.
## My Solve
**Flag:** 'pwn.college{Mu855UBBPD1L3p57vhoFcubrqio.QXxcDO0wSOxkjNzEzW}'

In this challenge, we simply had to use 'echo' to write the commands into a shell script 'x.sh'. Then we had to run it by using 'bash' command.
```
hacker@chaining~your-first-shell-script:~$ echo "/challenge/pwn; /challenge/college" > x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{Mu855UBBPD1L3p57vhoFcubrqio.QXxcDO0wSOxkjNzEzW}
```

## What I Learn
In order to save space in the terminal, we can store commands in a shell script and we can run it using 'bash' command.
## References
None.
