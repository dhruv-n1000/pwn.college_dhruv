## Detaching and attaching (tmux)
This challenge requires us to use 'tmux' to create terminal multiplexer.

### Solve
**Flag:** 'pwn.college{8XOVHgIyVQ9t5ee6GPs49kp-iuV.0VO4IDOxwSOxkjNzEzW}'

We had to use the 'tmux' command make multiple terminals by multiplexing, then we had to detach from it by using 'Ctrl-B + d'. Then we had to run /challenge/run which would 
put the flag in the tmux terminal, then we had to reatttach it by using 'tmux attach' and the terminal would have the flag.

```
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach

(inside tmux)
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ 11;rgb:0c0c/0c0c/0c0c echo Congratulations, here is your flag: pwn.college{8XOVHgIyVQ9t5ee6GPs49kp-iuV.0VO4IDOxwSOxkjNzEzW}

```

### What I Learnt
I learnt that we can use the 'tmux' command create virtual terminal inside your terminal. Its a modern alternative to 'screen' 
To detach from tmux, you press Ctrl-B followed by d.
The commands also differ:

1. tmux ls - List sessions
2. tmux attach or tmux a - Reattach to session
### References 
None. 
