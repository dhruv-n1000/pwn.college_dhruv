## Permission Tweaking Practice
We are supposed to add suid to the program and then read the flag. 

### Solve
**Flag:** 'pwn.college{wys6ZfvrwVzFQ1LWbE_j6r7tXxA.QXzEjN0wSOxkjNzEzW}'

I first added the suid to /challenge/getroot and then ran it, this spanned a root shell for me to cat /flag to get the flag.

```
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{wys6ZfvrwVzFQ1LWbE_j6r7tXxA.QXzEjN0wSOxkjNzEzW}
```

### What I Learnt
Learnt about SUID and how we can add SUID to a file as owners of the file so that other users can read the file. 
### References 
None. 
