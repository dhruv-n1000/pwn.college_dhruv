## Linking Files
The flag is in /flag but the program /challenge/catflag reads out /home/hacker/not-the-flag. We must use links so that the program reads the file with the flag 

## Solve
**Flag:** `pwn.college{UkjQHwp2eQI7E7Mjg2rAZfahDLE.QX5ETN1wSOxkjNzEzW}`

Since, the program /challenge/catflag only reads out /home/hacker/not-the-flag, I created a symbolic link with not-the-flag which made it linked to /flag. Hence when I run /challenge/catflag, it reads not-the-flag which links it to the /flag file hence giving me the flag. 

```
hacker@commands~linking-files:~$ rm /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{UkjQHwp2eQI7E7Mjg2rAZfahDLE.QX5ETN1wSOxkjNzEzW}
```

## New Learnings
Symbolic links are basically something that point to another file similar to shortcuts. I learnt about their applications and how they can be used. 

## References 
None.
