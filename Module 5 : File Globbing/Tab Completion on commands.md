# Tab Completion on commands
This challenge requires us to use auto-completion feature in the shell using tab key for commands unlike previous cases where 
we used it for file names.
## My Solve
**Flag:** 'pwn.college{0-3KjaBCv3_8erqxjQKlCQ_4oSV.0VN0EzNxwSOxkjNzEzW}'

In this challenge, we simply had to run a command that we know starts with 'pwncollege' but we do not know what comes after it.
So here we had to use tab key for completing the command name which gave us flag.
```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-8358
Correct! Here is your flag:
pwn.college{0-3KjaBCv3_8erqxjQKlCQ_4oSV.0VN0EzNxwSOxkjNzEzW}
```

## What I Learned
I learnt that we can use tab completion also for commands and not just files. Its useful when you are unaware of the command
name.
## References
None.
