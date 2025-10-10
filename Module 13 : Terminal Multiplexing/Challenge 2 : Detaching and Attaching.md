## Launching Screen
This challenge requires us to use detach from a particular screen and then reattach.

### Solve
**Flag:** 'pwn.college{oEEr6wGbe8e-PW5zrTksBwp-e91.0lN4IDOxwSOxkjNzEzW}'

We had to use the 'screen' command to create virtual terminal inside your terminal,then we had to detach from the virtual terminal by using 'Ctrl+D' and 'd' immediately after.
Then after we had detached, we had to run /challenge/run in the main terminal, which would send the flag back to the virtual terminal and then we had to attach back to the 
virtual terminal by using 'screen -r' which gave us the required flag.
```
hacker@terminal-multiplexing~detaching-and-attaching:~$
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{oEEr6wGbe8e-PW5zrTksBwp-e91.0lN4IDOxwSOxkjNzEzW}
Yes! Flag is: pwn.college{oEEr6wGbe8e-PW5zrTksBwp-e91.0lN4IDOxwSOxkjNzEzW}
```

### What I Learnt
I learnt that we can use the 'Ctrl+D' followed by 'd' to detach from a virtual terminal. Then we can attach the virtual terminal back again by using the '-r' argument along 
with the 'screen' command.
### References 
None. 
