## Handling Failure
This challenge requires us to use the '||' to chain 2 different commands.
## My Solve
**Flag:** 'pwn.college{co-Zx_-jTeoEPMGyWH3M-uknaRk.01M0MDOxwSOxkjNzEzW}'

In this challenge, we simply had to use '||' to chain 2 different executions. Here only if the first command ends in failure (exits with code not equal to 0), the second 
command is executed otherwise no.
```
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{co-Zx_-jTeoEPMGyWH3M-uknaRk.01M0MDOxwSOxkjNzEzW}
```

## What I Learn
I learnt that we can use '||', if we want the command to the right of the '&&' operator to run if and only if the command to the left of '&&' exits with exit code not equal to 0
(that is the first command is a failure).
## References
None.
