## Switching Windows (tmux)
We have two windows in the session where window 0 has the flag and window 1 is the welcome message. We must swtich windows to get the flag.

### Solve
**Flag:** 'pwn.college{Qya9MCq8vY4cq4z8mFCGuVdTLZD.0FM5IDOxwSOxkjNzEzW}'

Did the same as the previous switching windows challenge. I connected to the session made for us using tmux attach and switched to the welcome window which told me that
the flag is in window 0. I switched to window zero using ctrl+b and 0. This gave me the flag.

```
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach


(Window 1)
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Welcome to the tmux window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-B 0 to switch to window 0!
> MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!


(Window 0)
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{Qya9MCq8vY4cq4z8mFCGuVdTLZD.0FM5IDOxwSOxkjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{Qya9MCq8vY4cq4z8mFCGuVdTLZD.0FM5IDOxwSOxkjNzEzW}

```

### What I Learnt
Just the same as screen but with ctrl+B instead of Ctrl +A.
### References 
None.
