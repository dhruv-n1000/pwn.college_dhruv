# Hidden  Files
The challenge requires us to use the '-a' flag along with the ls command to see the hidden files in a directory that begin with '.'
## My Solve
**Flag:** 'pwn.college{QKuhXjoNSpyh58hrc25fvusTKAl.QXwUDO0wSOxkjNzEzW}'

In this challenge, We simply had to use the '-a' flag with ls command to view tha name of the hidden file containing the flag, then after discovering the name we had to run the file to get the key.
```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-274993027724881  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-274993027724881
pwn.college{QKuhXjoNSpyh58hrc25fvusTKAl.QXwUDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the '-a' flag with ls command to view all the files in a directory including the hidden ones which will not be visible using the simple ls command.
## References
None.
