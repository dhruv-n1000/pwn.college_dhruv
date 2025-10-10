## Building On Success
This challenge requires us to use the '&&' to chain 2 different commands.
## My Solve
**Flag:** 'pwn.college{sE1AVv1k1dz9VohnVjJMjPzKwPp.0lM0MDOxwSOxkjNzEzW}'

In this challenge, we simply had to use '&&' to chain 2 different executions. Here only if the first command is successful (exits with code 0), the second command is executed
otherwise no.
```
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{kWkLkkOSCJxbFlKpDwNeOLroz8B.QX1UDO0wSOxkjNzEzW}
hacker@chaining~chaining-with-semicolons:~$
Connected!
hacker@chaining~building-on-success:~$ /challenge/first-success
hacker@chaining~building-on-success:~$ /challenge/second
Error: /challenge/first-success must be successfully chained with
/challenge/second using &&
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{sE1AVv1k1dz9VohnVjJMjPzKwPp.0lM0MDOxwSOxkjNzEzW}
```

## What I Learn
I learnt that we can use '&&', if we want the command to the right of the '&&' operator to run if and only if the command to the left of '&&' exits with exit code 0 (that is
the first command is successful).
## References
None.
