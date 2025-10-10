## Reading Shell Scripts
This challenge requires us to read a shell script by using 'cat' followed by its name.
## My Solve
**Flag:** 'pwn.college{IoifinhuvsSjGehRmcLHAGZKXrd.0lMwgDOxwSOxkjNzEzW}'

In this challenge, we simply had to read a pre-existing shell script by using 'cat' followed by its name, it contained a password that was essential to run the shell script,
we had to find the password and then enter it while running to get the flag.
```
hacker@chaining~reading-shell-scripts:~$ cat /challenge/rum
cat: /challenge/rum: No such file or directory
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{IoifinhuvsSjGehRmcLHAGZKXrd.0lMwgDOxwSOxkjNzEzW}
```

## What I Learnt
I learnt that we can read a shell script by using 'cat' followed by its name.
## References
None.
