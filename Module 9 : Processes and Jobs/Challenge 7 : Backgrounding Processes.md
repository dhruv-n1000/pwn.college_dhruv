# Backgrounding Processes
This challenge requires us to use the 'bg' command to background a process that was suspended.
## My Solve
**Flag:** 'pwn.college{g9n1FcGdpgBWi9o2Be16ym38Jk-.QX3QDO0wSOxkjNzEzW}'

In this challenge, we simply had to firt suspend the process by using 'Ctrl+Z' then background it by using 'bg' command. Now 
the process is running in the background, we had to launch another'/challenge/run' which detects if there is another process
in the background and gives us the flag.
```
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         161 S+   bash /challenge/run
root         163 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         161 S    bash /challenge/run
root         171 S    sleep 6h
root         172 S+   bash /challenge/run
root         174 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{g9n1FcGdpgBWi9o2Be16ym38Jk-.QX3QDO0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can use the 'bg' command to background any command that we had once suspended because of ongoing issues.
None.
