# Killing Processes
This challenge requires us to use the 'kill' command to kill a spefic process.
## My Solve
**Flag:** 'pwn.college{YSLPALdBasG97RkARPPUYtCeZY-.QXyQDO0wSOxkjNzEzW}'

In this challenge, we simply had to use the 'kill' command and provide the PID (Process ID) of the '/challenge/dont_run' file's process. We could find the process ID of the 
process by using the 'ps -ef' command  and in the list getting the PID.
```
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 13:21 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 13:21 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 13:21 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 13:21 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 13:21 ?        00:00:00 sleep 6h
hacker       139       0  0 13:21 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       145     139  0 13:21 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       163       1  0 13:21 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --po
hacker       167     163  0 13:21 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       177       0  0 13:22 pts/2    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       183     177  0 13:22 pts/2    00:00:00 /run/dojo/bin/bash --login
hacker       192     183  0 13:22 pts/2    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill /challenge/dont_run
bash: kill: /challenge/dont_run: arguments must be process or job IDs
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{YSLPALdBasG97RkARPPUYtCeZY-.QXyQDO0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use the 'kill' command to kill any active process.
But the point to remember is that we dont provide the name of the process, we in fact provide the PID of the process which we can see clearly by using 'ps -ef' and then
grepping through the processes to get the required processs.
## References
None.
