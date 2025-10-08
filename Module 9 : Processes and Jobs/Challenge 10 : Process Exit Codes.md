# Starting Backgrounded Processes
We are to access the exit code of /challenge/get-code which as an argument to /challenge/submit-code will give the flag
## My Solve
**Flag:** 'pwn.college{w2L9cKgJE0_di2apqcO0E7IPapj.QX5YDO1wSOxkjNzEzW}'

I first ran the process /challenge.get-code which gave an error. On entering echo '$?' where '$' is used to access the value
of the variable '?' which is the variable for the exit code of the last terminated process. This gave me the exit code for the
first process which on using as the argument for the second process gave me the flag.
```
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
146
hacker@processes~process-exit-codes:~$ /challenge/submit-code 146
CORRECT! Here is your flag:
pwn.college{w2L9cKgJE0_di2apqcO0E7IPapj.QX5YDO1wSOxkjNzEzW}
```

## What I Learn
I learnt that exit codes of the last terminated program are stored in the variable ? and this variable can be read using 
various methods to access the exit code like by using '$' to access the value of a variable.
Eg. 'echo $?' gives us the exit code of the last terminated process.
## Reference
None.
