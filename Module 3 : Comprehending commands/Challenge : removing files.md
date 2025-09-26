# Removing Files
The challenge requires us to use the 'rm' command to delete a file from the home directory.
## My Solve
**Flag:** 'pwn.college{M9v66ypx_6_KQkwJ4p7bsndLxnU.QX2kDM1wSOxkjNzEzW}'

In this challenge, We simply had to use the 'rm' command to delete a file names 'delete_me' which was present in out home directory'
```
hacker@commands~removing-files:~$ ls
delete_me  o
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
o
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{M9v66ypx_6_KQkwJ4p7bsndLxnU.QX2kDM1wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'rm' command to remove a file from any directory.
## References
None.
