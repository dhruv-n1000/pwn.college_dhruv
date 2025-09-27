# Mixing Globs
This challenge requires us to put our knowledge of all the globs we have learnt so far to test. Among a lot of words in the directory,
we have to use globs in such a way that only 'challenging', 'educational' and 'pwning' are selected.
## My Solve
**Flag:** 'pwn.college{sFnQ8MRT8QhnbWWnf69v_uyR6aV.QX1IDO0wSOxkjNzEzW}'

In this challenge, we had to change our directory to '/challenge/files' and then run '/challenge/run' with providing a single argument: 
a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", 
"educational", and "pwning" only among all the available option.
```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ ls
amazing      delightful   great       jovial    magical     pwning   splendid   victorious  youthful
beautiful    educational  happy       kind      nice        queenly  thrilling  wonderful   zesty
challenging  fantastic    incredible  laughing  optimistic  radiant  uplifting  xenial
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{sFnQ8MRT8QhnbWWnf69v_uyR6aV.QX1IDO0wSOxkjNzEzW}
```

## What I Learned
I learnt how we can use logic to deduce how globs can be used strategically to save time while mentioning arguments, such that only 
required files stay eligible and all others are eliminated by the globs we use in the command argument.
## References
None.
