## Chaning File Ownership
This challenge requires us to use 'chown' command to change ownership of a particular file in linux subsystem.

### Solve
**Flag:** 'pwn.college{YKIUG4gCrP-vRLSwkE8wPGmG52-.QXxEjN0wSOxkjNzEzW}'

We had to use 'chmod' to change ownership of '/flag' from root to hacker (that is us), so that we can 'cat' the file and read the flag from it.

```
hacker@permissions~changing-file-ownership:~$ ls -l
total 32
-rw-r--r-- 1 hacker hacker   4 Sep 30 16:23 COLLEGE
-rw-r--r-- 1 hacker hacker   8 Sep 30 17:03 PWN
-rw-r--r-- 1 hacker hacker 829 Sep 30 16:55 instructions
-rw-r--r-- 1 hacker hacker  95 Sep 30 16:55 myflag
lrwxrwxrwx 1 hacker hacker   5 Sep 26 20:54 not-the-flag -> /flag
-rw-r--r-- 1 root   hacker  60 Sep 24 10:52 o
-rw-r--r-- 1 hacker hacker 437 Sep 30 16:38 the-flag
-rw-r--r-- 1 root   hacker  77 Sep 30 18:12 whatswrong
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{YKIUG4gCrP-vRLSwkE8wPGmG52-.QXxEjN0wSOxkjNzEzW}
```

### What I Learnt
I learnt how we can change ownership of a file to allow other users to access the file, it can typically be done only by 'root' user but for this challenge it was made usable
even by regular users.

### References 
None. 
