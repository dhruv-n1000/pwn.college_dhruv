# Comparing files.
The challenge requires us to use the 'diff' command to compare two files line by line and show you the exact difference between them.
For example:
```
hacker@dojo:~$ cat file1
hello
world
hacker@dojo:~$ cat file2
hello
universe
hacker@dojo:~$ diff file1 file2
2c2
< world
---
> universe
```
The output tells us that line 2 changed (2c2), with world in the first file (<) being replaced by universe in the second file (>).
Sometimes, when new lines are added, you'll see something like:
```
hacker@dojo:~$ cat old
pwn
hacker@dojo:~$ cat new
pwn
college
hacker@dojo:~$ diff old new
1a2
> college
```
This tells us that after line 1 in the first file, the second file has an additional line (1a2 means "after line 1 of file1, add line 2 of file2").
## My Solve
**Flag:** 'pwn.college{oHcpwIn8UtoCKRDdpqAeb4jm8wQ.01MwMDOxwSOxkjNzEzW}'

In this challenge, We simply had to use the 'diff' command to compare two files line by line, one file had 100 fake flags while the other one had 100 fake flags + 1 real flag which would be highlighted using the 'diff' command.
```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
51a52
> pwn.college{oHcpwIn8UtoCKRDdpqAeb4jm8wQ.01MwMDOxwSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'diff' command to compare 2 files line by line and know any difference in the 2 files. Also if one file has the contents of the other file plus some additional stuff, 'diff' command highlights that even.
## References
None.
