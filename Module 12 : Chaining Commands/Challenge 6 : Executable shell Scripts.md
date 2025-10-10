## Executable Shell Script
This challenge requires us to execute a shell script without using the bash command.
## My Solve
**Flag:** 'pwn.college{Y1Z8COWuLpn1Q2B6qRyxeNkzNle.QX0cjM1wSOxkjNzEzW}'

In this challenge, we simply had to use 'echo' to write the commands into a shell script 'x.sh'. Then we had to make it executable by using 'chmod'. Then we simple had to provide
its path and run it.
```
hacker@chaining~executable-shell-scripts:~$ echo "/challenge/solve" > abc.sh
hacker@chaining~executable-shell-scripts:~$ ls
COLLEGE  PWN  abc.sh  instructions  myflag  not-the-flag  o  shello.sh  the-flag  whatswrong  x.sh
hacker@chaining~executable-shell-scripts:~$ chmod ugo+x abc.sh
hacker@chaining~executable-shell-scripts:~$ abc.sh
bash: abc.sh: command not found
hacker@chaining~executable-shell-scripts:~$ ./abc.sh
Congratulations on your shell script execution! Your flag:
pwn.college{Y1Z8COWuLpn1Q2B6qRyxeNkzNle.QX0cjM1wSOxkjNzEzW}
```

## What I Learn
I learnt that we can run a shell script without using bash, we have to make the shell file executable by using 'chmod' and then we can simple execute it normally without needing
bash.
## References
None.
