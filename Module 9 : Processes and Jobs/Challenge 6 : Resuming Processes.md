# Resuming Processes
This challenge requires us to use the 'fg' command to resume a process that was suspended.
## My Solve
**Flag:** 'pwn.college{wGpecgBUU42E6bOeSqiHmslYm6l.QX2QDO0wSOxkjNzEzW}'

In this challenge, we simply had to firt suspend the process by using 'Ctrl+Z' then resume it by using 'fg' command and that
would give us the flag.
```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run
/challenge/run
I'm back! Here's your flag:
pwn.college{wGpecgBUU42E6bOeSqiHmslYm6l.QX2QDO0wSOxkjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I Learn
I learnt that we can use the 'fg' command to resume any command that we had once suspended because of ongoing issues.
None.
