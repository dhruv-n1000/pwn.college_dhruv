# Listing Processes
This challenge requires us to use the 'ps' command to list all the processes.
## My Solve
**Flag:** 'pwn.college{Uy2JYJqnTzlnvgrsFZwfufx44CC.QX4MDO0wSOxkjNzEzW}'

In this challenge, we simply had to use the 'ps' command with '-ef' argument, it will give us a list of all the processes currrently active in the terminal, it had the name 
of the file that contained the flag '/challenge/28817-run-25293'. Then we just had to run the file to get the flag.
```
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 13:06 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 13:06 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 13:06 ?        00:00:00 /challenge/28817-run-25293
root         135     132  0 13:06 ?        00:00:00 sleep 6h
hacker       146       1  0 13:06 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --po
hacker       150       0  0 13:06 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       156     150  0 13:06 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       166     156  0 13:07 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/28817-run-25293
Yahaha, you found me! Here is your flag:
pwn.college{Uy2JYJqnTzlnvgrsFZwfufx44CC.QX4MDO0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use the 'ps' command to list all the active processes.
As ps is a very old utility, its usage is a bit of a mess. There are two ways to specify arguments.
1. Standard Syntax: in this syntax, you can use -e to list "every" process and -f for a "full format" output, including arguments. These can be combined into a single
   argument -ef.
2.BSD Syntax: in this syntax, you can use a to list processes for all users, x to list processes that aren't running in a terminal, and u for a "user-readable" output.
  These can be combined into a single argument aux.
These two methods, ps -ef and ps aux, result in slightly different, but cross-recognizable output.
## References
None.
