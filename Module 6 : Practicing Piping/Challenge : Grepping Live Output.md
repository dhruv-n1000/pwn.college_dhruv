# Grepping Live Output
This challenge requires us to use the '|' (pipe) to take Standard output from the command to the left of the pipe and connect it to standard input of the command to the 
right of the pipe. 
## My Solve
**Flag:** 'pwn.college{IzE8p78Q7zIbr4NzDgFUh12bIO-.QX5EDO0wSOxkjNzEzW}'

In this challenge, we simply had to use '|' to connect the standard output from the command to the left of the pipe '/challenge/run' to the standard input of the command to
the right of the pipe 'grep'.
```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwning
pwns
pwn.college{IzE8p78Q7zIbr4NzDgFUh12bIO-.QX5EDO0wSOxkjNzEzW}
pwn
pwned
```

## What I Learned
I learnt that '|' (pipe) can be used to connect the standard output from the command to the left of the pipe to the standard input of the command to the right of the pipe.
## References
None.
