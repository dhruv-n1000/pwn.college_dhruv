## Finding Commands
This challenge requires us to use 'which' command to find the exact PATH of a particular command.

### Solve
**Flag:** 'pwn.college{05rZLEkUJFe_xRWItzfsijUtiJU.01NzEzNxwSOxkjNzEzW}'


We simply had to use 'which' command to find the PATH of the command 'win' then in the same directory as command, flag was also stored, we just had to 'cat' flag and get the 
flag.

```
hacker@path~finding-commands:~$ which win
/challenge/paths/17453/win
hacker@path~finding-commands:~$ ls /challenge/paths/17453
flag  win
hacker@path~finding-commands:~$ /challenge/paths/17453/flag
bash: /challenge/paths/17453/flag: Permission denied
hacker@path~finding-commands:~$ cat /challenge/paths/17453/flag
pwn.college{05rZLEkUJFe_xRWItzfsijUtiJU.01NzEzNxwSOxkjNzEzW}

```

### What I Learnt
I learnt that we can get the exact address of a command by using the 'which' command. 
### References 
None.
