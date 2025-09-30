# Redirecting Input
This challenge requires us to redirect input of a file to another file using '<'.
## My Solve
**Flag:** 'pwn.college{EBSZqKKhtfspc1G-YqMd0-K2EO2.QXwcTN0wSOxkjNzEzW}'

In this challenge, we simply had to use '<' to redirect the input of a file 'PWN' to a file '/challenge/run'. To put the content "COLLEGE" to 'PWN' we simply had to use '>'.
```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{EBSZqKKhtfspc1G-YqMd0-K2EO2.QXwcTN0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use '<' to redirect the input content of a file to another file.
## References
None.
