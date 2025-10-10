## Fun With Group Names
This challenge requires us to check our group name first and then use chgrp.

### Solve
**Flag:** 'pwn.college{I82YHvKLne5NY5W0Yjw-BOj7CpP.QXycjM1wSOxkjNzEzW}'

We had to use the 'id' command to check what group we are a part of and then use 'chgrp' command to change the group of '/fla' into our own group and then use the 'cat' 
command to read out the flag.

```
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp13147) groups=1000(grp13147)
hacker@permissions~fun-with-groups-names:~$ ls -l
total 32
-rw-r--r-- 1 hacker grp13147   4 Sep 30 16:23 COLLEGE
-rw-r--r-- 1 hacker grp13147   8 Sep 30 17:03 PWN
-rw-r--r-- 1 hacker grp13147 829 Sep 30 16:55 instructions
-rw-r--r-- 1 hacker grp13147  95 Sep 30 16:55 myflag
lrwxrwxrwx 1 hacker grp13147   5 Sep 26 20:54 not-the-flag -> /flag
-rw-r--r-- 1 root   grp13147  60 Sep 24 10:52 o
-rw-r--r-- 1 hacker grp13147 437 Sep 30 16:38 the-flag
-rw-r--r-- 1 root   grp13147  77 Sep 30 18:12 whatswrong
hacker@permissions~fun-with-groups-names:~$ /flag
bash: /flag: Permission denied
hacker@permissions~fun-with-groups-names:~$ chgrp grp13147 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{I82YHvKLne5NY5W0Yjw-BOj7CpP.QXycjM1wSOxkjNzEzW}
```

### What I Learnt
I Learnt how we can check what groups we are a part of by using 'id' command, and the rest was just an applicatio of previous challenge's concepts.
### References 
None. 
