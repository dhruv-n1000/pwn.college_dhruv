# Redirection Output
This challenge requires us to redirect stdout to files using '>' character. Then you can cat the output to see the file content.
## My Solve
**Flag:** 'pwn.college{I8fE7nU8qsNM5ZpiD_QMZuHvNQV.QX0YTN0wSOxkjNzEzW}'

In this challenge, we simply had to use '>' to redirect the stdout (PWN) to a file (COLLEGE) by using 'echo PWN > COLLEGE'.
```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{I8fE7nU8qsNM5ZpiD_QMZuHvNQV.QX0YTN0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use '>' to redirect the stdout to any file by using '>'.
## References
None.
