# Starting Backgrounded Processes
This challenge requires us to use the '&' operator while running a process so that the process can be run in the background.
## My Solve
**Flag:** 'pwn.college{cyQn82WY8fJTXhjYcOxhLtUcMA2.QX5QDO0wSOxkjNzEzW}'

In this challenge, we simply had to start a process in the background by using the '&' operator in this way : 
'/challenge/run &'
```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 164
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{cyQn82WY8fJTXhjYcOxhLtUcMA2.QX5QDO0wSOxkjNzEzW}

[1]+  Done                    /challenge/run
```

## What I Learn
I learnt that we can use the '&' operator while running a process so that we start running a process in the background itself.
Earlier we were backgrounding a suspended or foreground running process, but now we are starting the process itself in the
background.
## Reference
None.
