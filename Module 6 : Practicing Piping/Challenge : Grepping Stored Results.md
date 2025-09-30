# Grepping Stored Results
This challenge requires us to put our combined knowledge of running a file, redirecting its output and searching for contents of a file to test.
## My Solve
**Flag:** 'pwn.college{A-uPHiDaVJQG161NrcXHfa6NPZ5.QX4EDO0wSOxkjNzEzW}'

In this challenge, we simply had to use '>' to redirect the stdout of a file '/challenge/run' to '/tmp/data.txt', then we had to search for the flag from hundreds of lines
of content in '/tmp/data.txt' using 'grep' command.
```
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwning
pwn.college{A-uPHiDaVJQG161NrcXHfa6NPZ5.QX4EDO0wSOxkjNzEzW}
pwn
pwned
pwns
```

## What I Learned
I revised my previous 'grep' command concept and saw how we can use three different teachings in a single case scenario.
## References
None.
