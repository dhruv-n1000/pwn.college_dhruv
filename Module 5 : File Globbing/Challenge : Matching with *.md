# Matching with *
The challenge requires us to use a glab '*'. When it encounters a '*' character in any argument, the shell will treat it as a wildcard and try to replace that argument
with any files that match the pattern.
## My Solve
**Flag:** 'pwn.college{4qSp9huvtvAxb1Fkk94WzHa7imL.QXxIDO0wSOxkjNzEzW}'

In this challenge, we had to change our directory to '/challenge' but we had to keep our total character input less than 4, so we had to basically use glob '*' to help reduce the
characters. After we are in the directory '/challenge' we had to just run '/challenge/run' to get the flag.
```
hacker@globbing~matching-with-:~$ cd /c*e
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{4qSp9huvtvAxb1Fkk94WzHa7imL.QXxIDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the glob '*'. When it encounters a '*' character in any argument, the shell will treat it as a wildcard and try to replace that argument
with any files that match the pattern. The '*' matches any part of the filename except for / or a leading . character.
For instance : 
'cd /c*e' is understood by the shell as 'cd /challenge' because of '*' glob used.
## References
None.
