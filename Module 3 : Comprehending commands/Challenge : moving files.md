# Moving Files
The challenge requires us to use the 'mv' command to move file content of one file to another.
## My Solve
**Flag:** 'pwn.college{4G3C0uuE5zhjakBc25CwOA-bJPF.0VOxEzNxwSOxkjNzEzW}'

In this challenge, We simply had to use the 'mv' command to move contents of '/flag' to '/tmp/hack-the-planet' and then run the file '/challenge/check' for the website to check if we did it and give the flag.
```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{4G3C0uuE5zhjakBc25CwOA-bJPF.0VOxEzNxwSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'mv' command to move contents of 1 file to another byusing 'mv file1 file2'
## References
None.
