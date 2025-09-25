# Listing Files
The challenge requires us to use the 'ls' command to list all the files or directories in a particular directory. 
## My Solve
**Flag:** 'pwn.college{EDIITjXno5uTD98hC6SKVm7ZEbl.QX4IDO0wSOxkjNzEzW}'

In this challenge, We simply had to use the 'ls' command to list all the files in the directory '/challenge' and in that directory there was a file with an unusual name which contained the flag, so after listing we had to open the weird named file to get the flag
```
hacker@commands~listing-files:~$ ls /challenge
6910-renamed-run-15007  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/6910-renamed-run-15007
Yahaha, you found me! Here is your flag:
pwn.college{EDIITjXno5uTD98hC6SKVm7ZEbl.QX4IDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'ls' command to list all the files belonging in a particular directory.
## References
None.
