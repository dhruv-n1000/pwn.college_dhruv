## Setting PATH
This challenge requires us to set the value of PATH variable to a directory.

### Solve
**Flag:** 'pwn.college{MgJh_Hf0EZmEmEmQ9NHQb6Fg3ne.QX1cjM1wSOxkjNzEzW}'


We simply had to set the value of PATH="/challenge/more_commands/" and then run /challenge/run which would invoke the win command which would be found in the PATH mentioned 
above only, if the win command is invoked, it gives us the flag.
```
hacker@path~setting-path:~$ PATH="/challenge/more_commands/"
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{MgJh_Hf0EZmEmEmQ9NHQb6Fg3ne.QX1cjM1wSOxkjNzEzW}

```

### What I Learnt
I learnt that we can set the value of PATH to any directory, which will come useful if we want to access something from that directory.
### References 
None.
