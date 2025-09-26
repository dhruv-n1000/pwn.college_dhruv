# Making Directories
The challenge requires us to use the 'mkdir' command to create a new directory.
## My Solve
**Flag:** 'pwn.college{MvrHKURtYJgH4QrTthrwWkJvDcj.QXxMDO0wSOxkjNzEzW}'

In this challenge, We simply had to use the 'mkdir' command to create a new directory called 'pwn' in the directory 'tmp' and then create a new file inside 'pwn' using 'touch' command. Then we were required to run '/challenge/run' so that it could check if we completed the challenge.
```
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  tmp.4mK6TfTSUV
hacker@commands~making-directories:/tmp$ mkdir  pwn
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{MvrHKURtYJgH4QrTthrwWkJvDcj.QXxMDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'mkdir' command to create a new directory in a directory.
## References
None.
