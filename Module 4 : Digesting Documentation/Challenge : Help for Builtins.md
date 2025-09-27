# help For Builtins
The challenge aims to teach us about some commands which rather than being programs with 'man' pages and 'help' options, are built 
into the  shell itself. These are called builtins. Also we have 'help' builtin to search for help in such builtin programs.
## My Solve
**Flag:** 'pwn.college{4o5OIjkR34B9Ew5Vcch3l7E0TzS.QX0ETO0wSOxkjNzEzW}'

In this challenge, our challenge command was made a builti rather than a regular program. So this would not have 'man' or '--help' work.
Hence we had to use the builtin 'help' to look up the help of 'challenge' to figure out the right argument to pass along with challenge
to get the flag.
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "4o5OIjkR".
hacker@man~help-for-builtins:~$ challenge --secret 4o5OIjkR
Correct! Here is your flag!
pwn.college{4o5OIjkR34B9Ew5Vcch3l7E0TzS.QX0ETO0wSOxkjNzEzW}
```

## What I Learned
I learnt that some commands which rather than being programs with 'man' pages and 'help' options, are built into the  shell itself.
These are called builtins. Also we have 'help' builtin to search for help in such builtin programs.
## References
None.
