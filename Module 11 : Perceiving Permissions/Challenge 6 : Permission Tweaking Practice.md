## Permission Tweaking Practice
This challenge requires us to use our knowledge of changing file permissions to solve an 8 round game.

### Solve
**Flag:** 'pwn.college{kdey_2-WiS5aRXvaWbw56MLZ4fn.QXwEjN0wSOxkjNzEzW}'

We had to use the 'chmod' command to change file permissions as per the round's demand every time to advance to the next round. When all the rounds were over, we had to make
'/flag' readable by using 'chmod ugo+r /flag'. Then we simply had to read the flag from that.

```
hacker@permissions~permission-tweaking-practice:~$ /challenge/run
Round 1 of 8!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-rw-rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod go+w /challenge/pwn
You set the correct permissions!
Round 2 of 8!

Current permissions of "/challenge/pwn": rw-rw-rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": r--r--rw-
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod ug-w /challenge/pwn
You set the correct permissions!
Round 3 of 8!

Current permissions of "/challenge/pwn": r--r--rw-
* the user does have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-r--rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod u+w /challenge/pwn
You set the correct permissions!
Round 4 of 8!

Current permissions of "/challenge/pwn": rw-r--rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-r--rwx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod o+x /challenge/pwn
You set the correct permissions!
Round 5 of 8!

Current permissions of "/challenge/pwn": rw-r--rwx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rw-r-xrwx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod g+x /challenge/pwn
You set the correct permissions!
Round 6 of 8!

Current permissions of "/challenge/pwn": rw-r-xrwx
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod u+x,g+w /challenge/pwn
You set the correct permissions!
Round 7 of 8!

Current permissions of "/challenge/pwn": rwxrwxrwx
* the user does have read permissions
* the user does have write permissions
* the user does have execute permissions
* the group does have read permissions
* the group does have write permissions
* the group does have execute permissions
* the world does have read permissions
* the world does have write permissions
* the world does have execute permissions

Needed permissions of "/challenge/pwn": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod ugo-rwx /challenge/pwn
You set the correct permissions!
Round 8 of 8!

Current permissions of "/challenge/pwn": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": ---r-xr-x
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
* the group does have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
* the world does have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod go+rx /challenge/pwn
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!

Current permissions of "/flag": ---------
- the user doesn't have read permissions
- the user doesn't have write permissions
- the user doesn't have execute permissions
- the group doesn't have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
- the world doesn't have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions
hacker@permissions~permission-tweaking-practice:~$ chmod ugo+r /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{kdey_2-WiS5aRXvaWbw56MLZ4fn.QXwEjN0wSOxkjNzEzW}
```

### What I Learnt
We revised previous topics in a game format.
### References 
None. 
