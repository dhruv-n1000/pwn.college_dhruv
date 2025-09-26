# Touching Files
The challenge requires us to use the 'touch' command to create an empty file in a directory.
## My Solve
**Flag:** 'pwn.college{ASdGkuhM0j5JGbg88p2s1Nu-v05.QXwMDO0wSOxkjNzEzW}'

In this challenge, We simply had to use the 'touch' command to create 2 blank files '/tmp/pwn' and '/tmp/college' and then simple execute the '/challenge/run' to get the flag.
```
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ ls
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{ASdGkuhM0j5JGbg88p2s1Nu-v05.QXwMDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'touch' command to create an empty file in a directory.
## References
None.
