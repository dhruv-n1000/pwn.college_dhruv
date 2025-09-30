# Grepping Errors
This challenge requires us to use 'grep' command to search for something within the 'error' of a particular file whilst using the '|'. But '|' only connects standard output of
one file to standard input of another and not errors. We can use '>&' in this case which redirects a file descriptor to another file descriptor, hence we redirect errors of a 
file to output descriptor of the same file and then use '|'.
## My Solve
**Flag:** 'pwn.college{AAQIbFFXnk4TbzXK9GAuIEMS7C3.QX1ATO0wSOxkjNzEzW}'

In this challenge, we simply had to use '>&' command to redirect the error of '/challenge/run' to output of the same by using '/challenge/run 2>& 1' then we could ue the '|'
as the contents of error lie in output which could be connected to the right lying command's input. We use grep to find 'pwn' and get the flag.
```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwned
pwn.college{AAQIbFFXnk4TbzXK9GAuIEMS7C3.QX1ATO0wSOxkjNzEzW}
pwning
pwns
pwn
```

## What I Learn
I learnt that we can use '>&' command to redirect a file descriptor to another file descriptor. We can redirect standard error to standard output by using '2>& 1'. 
Then this can be easily by connected using pipe (|) for 'grepping' through it.
## References
None.
