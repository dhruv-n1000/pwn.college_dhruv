## Switching Windows
This challenge requires us to switch windows inside a screen using shortcuts.

### Solve
**Flag:** 'pwn.college{MByeXJ5yiEn2R_qGBurJjrIRqVZ.0FO4IDOxwSOxkjNzEzW}'

We had to use the 'screen -ls' to look at all the ID of the screen, then we had to open the screen by using 'screen -r ID'. It took us to the Window 1, there we had to use 
'Ctrl-A + 0' to hop onto the Window 0 which gave us the flag.

```
hacker@terminal-multiplexing~switching-windows:~$ screen -ls
There are screens on:
        173.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        144.session_7d95abb08a88add5    (Remote or dead)
        147.session_2a67fb5993a5eb5b    (Remote or dead)
        150.session_3479f20dcdc4de69    (Remote or dead)
        147.session_3904159af30b6f1b    (Remote or dead)
        150.session_546983c552cedc03    (Remote or dead)
        135.challenge_session   (Detached)
7 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~switching-windows:~$ screen -r 135


(Window 1)

Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Welcome to the window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-A 0 to switch to window 0!
> MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows:~$


(Window 0)

hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{MByeXJ5yiEn2R_qGBurJjrIRqVZ.0FO4IDOxwSOxkjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{MByeXJ5yiEn2R_qGBurJjrIRqVZ.0FO4IDOxwSOxkjNzEzW}
```

### What I Learnt
I learnt that we can use various key combinations followed by a character to perform switching tasks among the windows of a screen.
These windows are handled with different keyboard shortcuts, all starting with Ctrl-A:

Ctrl-A c - Create a new window
Ctrl-A n - Next window
Ctrl-A p - Previous window
Ctrl-A 0 through Ctrl-A 9 - Jump directly to window 0-9
Ctrl-A " - bring up a selection menu of all of the windows
### References 
None. 
