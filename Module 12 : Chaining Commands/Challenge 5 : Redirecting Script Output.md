## Redirecting Script Output
This challenge requires us to pipe the output of a shell script into a new program.
## My Solve
**Flag:** 'pwn.college{Q2rJUoCRqgWco56sq1Fhc-mZiyU.QX4ETO0wSOxkjNzEzW}'

In this challenge, we simply had to use 'echo' to write the commands into a shell script 'x.sh'. Then we had to pipe its output by using 'bash' command and '|' into a different
file.
```
hacker@chaining~redirecting-script-output:~$ echo "/challenge/pwn; /challenge/college" > x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{Q2rJUoCRqgWco56sq1Fhc-mZiyU.QX4ETO0wSOxkjNzEzW}
```

## What I Learn
I Learnt that we can take the output of an enitre shell script, use it as a command in order to pipe it into the '|' and put it into a different command alltogether.
## References
None.
