# Interrupting Processes
This challenge requires us to use the hotkey for Interrupring a process. Terminals have builtin 'Ctrl+C' for this, doing this sends an interrupt signal to the current 
running process. 
## My Solve
**Flag:** 'pwn.college{w9TD8gX7W15SbMd-pUD3cUjqwzf.QXzQDO0wSOxkjNzEzW}'

In this challenge, we simply had to use the 'Ctrl+C' hotkey after running '/challenge/run' to interrupt the process of running the '/challenge/run'. On interruption, we get 
the flag.
```
hacker@processes~interrupting-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 13:30 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 13:30 ?        00:00:00 /run/dojo/bin/sleep 6h
hacker       131       0  0 13:30 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       137       0  0 13:30 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       145       1  0 13:30 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --po
hacker       148     131  0 13:30 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       150     137  0 13:30 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       167     145  0 13:30 pts/2    00:00:00 /run/dojo/bin/bash --login
hacker       177       0  0 13:31 pts/3    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       183     177  0 13:31 pts/3    00:00:00 /run/dojo/bin/bash --login
hacker       198       0  0 13:32 pts/4    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       204     198  0 13:32 pts/4    00:00:00 /run/dojo/bin/bash --login
hacker       213     204  0 13:32 pts/4    00:00:00 ps -ef
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{w9TD8gX7W15SbMd-pUD3cUjqwzf.QXzQDO0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use the 'Ctrl+C' hotkey for Interrupring a process. 
Ctrl-C (e.g., holding down the Ctrl key and pressing C) sends an "interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the
application to cleanly exit.
## References
None.
