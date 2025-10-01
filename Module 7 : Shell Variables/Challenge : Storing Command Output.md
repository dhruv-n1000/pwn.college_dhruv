# Storing Command Outputs
This challenge requires us to use Command Substitution.
## My Solve
**Flag:** 'pwn.college{0aMLh12SsEBBtGHkMD9ZHWsUmJl.QX1cDN1wSOxkjNzEzW}'

In this challenge, we simply had to Read the output of the /challenge/run command directly into a variable called PWN, and
it will contain the flag.
```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{0aMLh12SsEBBtGHkMD9ZHWsUmJl.QX1cDN1wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use Command Substitution to store the output of some command into a variable.
eg1 : (we store content of a file by using cat)
hacker@dojo:~$ FLAG=$(cat /flag)
hacker@dojo:~$ echo "$FLAG"
pwn.college{blahblahblah}
eg2 : (we store output of a command by running it)
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{0aMLh12SsEBBtGHkMD9ZHWsUmJl.QX1cDN1wSOxkjNzEzW}
## References
None.
