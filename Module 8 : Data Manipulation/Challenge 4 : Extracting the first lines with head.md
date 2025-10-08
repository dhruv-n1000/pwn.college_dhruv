# Extracting the first lines with head
This challenge requires us to use the 'head' command to display the first few lines of output of a particular command.
## My Solve
**Flag:** 'pwn.college{QS6_j59-cZCXSjLZO5UdjQQRoHy.0lNxEzNxwSOxkjNzEzW}'

In this challenge, we simply had to use 'head' command to pipe the first 7 lines of the /challenge/run into /challenge/college.
```
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{QS6_j59-cZCXSjLZO5UdjQQRoHy.0lNxEzNxwSOxkjNzEzW}
```

## What I Learnt
The head command is used to display the first few lines of its output. By default, it shows the first 10 lines, but you can control this with the '-n'operator.
Eg : cat /something/very/long | head -n 2
    this 
    is
## Reference
None.
