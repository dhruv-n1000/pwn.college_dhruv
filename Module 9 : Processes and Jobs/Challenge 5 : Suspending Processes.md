# Suspending Processes
This challenge requires us to use the Ctrl+Z to suspend an ongoing process.
## My Solve
**Flag:** 'pwn.college{wP6SXTk-RlU4W6j48PXqV7Rrv0r.QX1QDO0wSOxkjNzEzW}'

In this challenge, we simply had to use the Ctrl+Z to suspend the process '/challenge/run' and re run it while the first one
is still suspended, and this would give u the flag.
```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     129  0 06:12 pts/0    00:00:00 bash /challenge/run
root         163     161  0 06:12 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     129  0 06:12 pts/0    00:00:00 bash /challenge/run
root         168     129  0 06:12 pts/0    00:00:00 bash /challenge/run
root         170     168  0 06:12 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{wP6SXTk-RlU4W6j48PXqV7Rrv0r.QX1QDO0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use the 'Ctrl+Z' key to suspend an ongoing process as and when such situation arises.
## References
None.
