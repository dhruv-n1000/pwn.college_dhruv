# Home Sweet Home
The challenge /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

1.Your argument must be an absolute path. 
2.The path must be inside your home directory. 
3.Before expansion, your argument must be three characters or less.

We thus have to specify our path as an arguement to /challenge/run
## My Solve
**Flag:** 'pwn.college{QC4QwYIHIP9UqEhGwgJEiWi2Ae4.QXzMDO0wSOxkjNzEzW}'

Here I entered ~o as an absolute path to /challenge/run for it to recieve the path and write the path in the file o. Here ~o is expanded as /home/hacker/o
```
hacker@paths~home-sweet-home:~$ /challenge/run ~/o
Writing the file to /home/hacker/o!
... and reading it back to you:
pwn.college{QC4QwYIHIP9UqEhGwgJEiWi2Ae4.QXzMDO0wSOxkjNzEzW}
```

## What I Learned
I learnt how we can use shell expansion in Linux commands, and how ~ refers to the home directory (in this case /home/hacker). Also if we use ~ twice only the first ~ is taken as home directory and the other one is kept as it it.
## References
None.
