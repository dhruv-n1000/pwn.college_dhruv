## Using Sudo
This challenge requires us to use sudo to become root.

### Solve
**Flag:** 'pwn.college{MYZv7WqJQVjSt7tdaHcKDcaNYLp.QX4UDN1wSOxkjNzEzW}'

We had to enter 'sudo' before every command so that the terminal knows that we are authorised to become root. 

```
hacker@users~using-sudo:~$ sudo ls
COLLEGE  PWN  instructions  myflag  not-the-flag  o  the-flag  whatswrong
hacker@users~using-sudo:~$ sudo not-the-flag
sudo: not-the-flag: command not found
hacker@users~using-sudo:~$ sudo cat not-the-flag
pwn.college{MYZv7WqJQVjSt7tdaHcKDcaNYLp.QX4UDN1wSOxkjNzEzW}
```

### What I Learnt
I Learnt how sudo (recent one) uses policies to determine whether the user is authorized to run commands as root or not as opposed to su (older one) which requires passwords
which can be easily leaked.

### References 
None. 
