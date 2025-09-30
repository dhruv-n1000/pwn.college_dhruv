# Redirecting More Output
This challenge requires us to redirect the output of 1 command to a file.
## My Solve
**Flag:** 'pwn.college{AYWnSnO3usYF9OBm3t2TzEm8UAb.QX1YTN0wSOxkjNzEzW}'

In this challenge, we simply had to use '>' to redirect the output of a command '/challenge/run' to a file 'myflag'. Then we had to 'cat' the file to get the desired flag.
```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{AYWnSnO3usYF9OBm3t2TzEm8UAb.QX1YTN0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use '>' to redirect the output of any command to a file.
## References
None.
