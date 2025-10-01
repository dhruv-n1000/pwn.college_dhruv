## Duplicating Piped Data With Tee
This challenge requires us to use the 'tee' command to duplicate the data passing through your pipe (|) into any number of files mentioned after 'tee'. This is useful in case
the program is not running and we need to debug.
## My Solve
**Flag:** 'pwn.college{4d0wqDNx7lF_rmX7QT6kJOsn3uj.QXxITO0wSOxkjNzEzW}'

In this challenge, we simply had to use 'tee' command to duplicate the data passing through the pipe into any file (in this case i used 'whatswrong'). Here data from output
of '/challenge/pwn' was being piped to input of '/challenge/college' but there was a missing argument, for that we used 'tee' to pass the data being piped to a third file, 
and then we 'cat' the file to debug the issue and see what is wrong.
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee whatswrong | /challenge/college
Processing...
WARNING: you are overwriting file whatswrong with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat whatswrong
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "4d0wqDNx"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret 4d0wqDNx | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{4d0wqDNx7lF_rmX7QT6kJOsn3uj.QXxITO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we could use 'tee' command to duplicate the data passing through the pipe (from one file's output to another file's input) into whatever number of files mentioned
after the 'tee' command.
Eg: we can duplicate file content into multiple files using 
'/challenge/pwn | tee whatswrong needhelp tryingtodebug'
where the pipe content is duplicated to three files : 'whatswrong', 'needhelp' and 'tryingtodebug'.
## References
None.
