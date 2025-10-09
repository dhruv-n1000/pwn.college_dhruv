## Other users with su
In this challenge we have to switch to another user using su and then run a program to get the flag. 

### Solve
**Flag:** 'pwn.college{ECcAkPYHz2Tx3vtML51L1F8C09o.QX2UDN1wSOxkjNzEzW}'

Here, we had to enter su with the argument of zardus i.e, the user we wanted to switch to and then we had to enter the user's password. I then ran the program /challenge/run to 
get the flag. 

```
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{ECcAkPYHz2Tx3vtML51L1F8C09o.QX2UDN1wSOxkjNzEzW}
```

### New Learnings
I learnt how su with an argument lets us change to specific users instead of just the root. 

### References 
None. 
