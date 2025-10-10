## Executable Files
This challenge requires us to change the executable permission of a file by using 'chmod'.

### Solve
**Flag:** 'pwn.college{Eoq1CRBVpTaU49iTeHh9Mctv6XR.QXyEjN0wSOxkjNzEzW}'

We had to use the 'chmod' command to make '/challenge/run' executable by owners, group members and others. Then execute the file to get the flag.

```
hacker@permissions~executable-files:~$ chmod ugo+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{Eoq1CRBVpTaU49iTeHh9Mctv6XR.QXyEjN0wSOxkjNzEzW}
```

### What I Learnt
I Learnt how we can change executable permissions of a file.
### References 
None. 
