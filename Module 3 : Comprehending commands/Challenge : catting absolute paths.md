# Catting Absolute Paths.
The challenge requires us to use the 'cat' command to read out files. In this case the flag for the challenge would be stored in a file called flag which we have to access using the entire absolute path.
## My Solve
**Flag:** 'pwn.college{catCnUnA8odCuvAMxGWIImO0ch0.QX5ETO0wSOxkjNzEzW}'

In this challenge, We simply had to use the 'cat' command to view the contents of the file 'flag' which was containing the flag we needed to pass the challenge but we had to provide the absolute patha as the argument.
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{catCnUnA8odCuvAMxGWIImO0ch0.QX5ETO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can also use the 'cat' command by giving the argument as a absolute path of the file we want to read.
## References
None.
