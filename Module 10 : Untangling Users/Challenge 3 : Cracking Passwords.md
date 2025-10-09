## Cracking Passwords
This challenge requires us to use 'john' command to get the leaked file's encrypted password converted to normal password.

### Solve
**Flag:** 'pwn.college{cj78HYqhwpqzaYhR2J5ROa40Gfw.QX3UDN1wSOxkjNzEzW}'

We had to use the john command and then type the name of the leaked password file so that it decrypts the encrypted password, then we just had to use su to enter the system 
as zardus, use the password we just got and then execute the 'challenge/run' command.

```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:23 100% 2/3 0.04345g/s 253.0p/s 253.0c/s 253.0C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{cj78HYqhwpqzaYhR2J5ROa40Gfw.QX3UDN1wSOxkjNzEzW}
```

### What I Learnt
I Learnt how we can crack passwords of various users in case we do not know the passwords beforehand, we just need to look for a leaked password file and then use the 
'john' command in it to get the password decrypted fro within the file.

### References 
None. 
