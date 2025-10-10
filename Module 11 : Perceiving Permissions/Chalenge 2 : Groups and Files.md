## Groups and Files
This challenge requires us to change the group of a particular file using 'chgrp'.

### Solve
**Flag:** 'pwn.college{0SlOOAKNQ4GDXcx2_wpK9TYxQm8.QXxcjM1wSOxkjNzEzW}'

We had to use the 'chgrp' command to change the group of '/flag' from 'root' to 'hacker' so that we could access the file as hacker user. For this challenge, usage of 'chgrp'
command was also given to the hacker user but in real life it can only be used by 'root' user.

```
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{0SlOOAKNQ4GDXcx2_wpK9TYxQm8.QXxcjM1wSOxkjNzEzW}
```

### What I Learnt
I Learnt how we can change group of a particular file to allow it to be accesible by all member users of that group, the usability of the command 'chgrp' is limited usually to 
only the 'root' user but in this challenge it was made usable by even 'hacker' user for the sake of challenge.
### References 
None. 
