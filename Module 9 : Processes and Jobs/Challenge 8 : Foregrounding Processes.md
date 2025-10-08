# Foregrounding Processes
This challenge requires us to use the 'fg' command to foreground a process that was backgrounded.
## My Solve
**Flag:** 'pwn.college{0aaXJXnQ5fAGyuN20gV9zkxEXDz.QX4QDO0wSOxkjNzEzW}'

In this challenge, we simply had to first suspend the process by using 'Ctrl+Z' then background it by using 'bg' command, once
it was backgrounded we had to use the 'fg' command to foreground the process and it would give us the flag.
```
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg /challenge/run
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{0aaXJXnQ5fAGyuN20gV9zkxEXDz.QX4QDO0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use the 'fg' command to foreground any process that was once backgrounded. Thus we can use 'fg' to either
foreground a backgrounded process or even resume a suspended process in foreground and not in the background.
None.
