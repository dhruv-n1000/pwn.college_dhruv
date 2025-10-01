## Writing To Multiple Programs
This challenge requires us to use the '>(command)' for writing to a command, the data goes to the standard input of the file.
**Flag:** 'pwn.college{8OT5ltOIMTgBhW2KW_ucWb0CMwY.QXwgDN1wSOxkjNzEzW}'

In this challenge, we simply had to  Run the /challenge/hack command, and duplicate its output as input using '>(command)' to both the /challenge/the and the 
/challenge/planet commands.
```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) >( /challenge/planet )
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
2707829286529416860
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{8OT5ltOIMTgBhW2KW_ucWb0CMwY.QXwgDN1wSOxkjNzEzW}
```

## What I Learned
I learnt that we could use '>(commandname)' for writing into a command (output process substitution), When commands write to this file, the data goes to the standard 
input of the command. Using '<(commandname)', we can read from output of the commandname (and not the data of command) while using '>(commandname)' we can write into the 
command.
## References
None.
