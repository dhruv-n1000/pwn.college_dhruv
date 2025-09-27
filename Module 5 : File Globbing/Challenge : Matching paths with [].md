# Matching paths with []
The challenge requires us to use a glab '[]'. When it encounters a '[]' character in any argument, the shell will treat it as a wildcard "single character" and try to replace
that argument with any any of the characters placed in '[]' if they are present in any files that match the pattern. In this one we have to enter absolute paths.
## My Solve
**Flag:** 'pwn.college{cTTF1QVhuxJ-By1e5MX1kst5ghj.QX0IDO0wSOxkjNzEzW}'

In this challenge, we had to write the command 'challenge/run' from the home directory itself. Since we were writing from home directory itself, in the globbing part where we
mention the general name of file we had to put the absolute path, '/challenge/files/file_[bash]'.
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{cTTF1QVhuxJ-By1e5MX1kst5ghj.QX0IDO0wSOxkjNzEzW}
```

## What I Learned
We can also use the glob '[]', to run programs remotely by using it in the path of the file while writing the run statement.
## References
None.
