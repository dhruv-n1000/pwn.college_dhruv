# Matching with ?
The challenge requires us to use a glab '?'. When it encounters a '?' character in any argument, the shell will treat it as a wildcard "single character" and try to replace
that argument with any files that match the pattern.
## My Solve
**Flag:** 'pwn.college{kF5546wUUKM2NUyyoAjwhl8zbn-.QXyIDO0wSOxkjNzEzW}'

In this challenge, we had to change our directory to '/challenge' but we had to use '?' glob instead of 'c' and 'l' in the word 'challenge'. After we are in the directory
'/challenge' we had to just run '/challenge/run' to get the flag.
```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kF5546wUUKM2NUyyoAjwhl8zbn-.QXyIDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the glob '?'. When it encounters a ? character in any argument, the shell will treat it as a single-character wildcard. This works like *, but only 
matches one character. 
For instance : 
'cd /abc' can be written using '?' as 'cd /a?c' but 'cd /love' cannot be written as 'cd /l?e' (unlike the '*" glob).
## References
None.
