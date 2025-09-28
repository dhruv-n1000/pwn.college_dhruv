# Tab Completion
This challenge requires us to use auto-completion feature in the shell using tab key.
## My Solve
**Flag:** 'pwn.college{4c7EDGHi7UNxlB-fYaAT8vJudfT.0FN0EzNxwSOxkjNzEzW}'

In this challenge, the flag was given in '/challenge/pwncollege', but we had to 'cat' this file not by typing out its name but
by using tab completion that is type 'p' or 'pw' etc and press tab.
```
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{4c7EDGHi7UNxlB-fYaAT8vJudfT.0FN0EzNxwSOxkjNzEzW}
```

## What I Learned
I learnt that we can use tab to autocomplete the commands that we have to type and its less error prone than using '*' glob.
## References
None.
