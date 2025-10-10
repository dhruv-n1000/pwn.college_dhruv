## Finding Sessions
This challenge requires us to find the right screen to reattach into after having multiple screens detached.

### Solve
**Flag:** 'ppwn.college{8LdNkia4JH43ll2wknfc6-pV0WU.01N4IDOxwSOxkjNzEzW}'

We had to use the 'screen -ls' command to first look at all the detached screens and then decide which one we have to open first. Then we use 'screen -r' and provide a screen's
id or username as argument to open the screen. Eventually one screen will be right.

```
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        173.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        144.session_7d95abb08a88add5    (Remote or dead)
        147.session_2a67fb5993a5eb5b    (Remote or dead)
        150.session_3479f20dcdc4de69    (Remote or dead)
        144.session_5a6bb274ee1e1bb0    (Detached)
        147.session_3904159af30b6f1b    (Detached)
        150.session_546983c552cedc03    (Detached)
7 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144

(in screen)
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{8LdNkia4JH43ll2wknfc6-pV0WU.01N4IDOxwSOxkjNzEzW}
pwn.college{8LdNkia4JH43ll2wknfc6-pV0WU.01N4IDOxwSOxkjNzEzW}
```

### What I Learnt
I learnt that we can use the 'screen -ls' command to have a look at the condition of all the screens. Also I learnt if we have multiple screens that could be atached, then we
use 'screen -r (screenname or screenID)' to open a particular screen.
### References 
None. 
