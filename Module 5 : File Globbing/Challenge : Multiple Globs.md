# Multiple Globs
This challenge requires us to use multiple globs in a single statement as opposed to what we have been doing so far ( use one glob at a time ).
## My Solve
**Flag:** 'pwn.college{gyjBd098ta-9eenzfm7v5qcHeb1.0lM3kjNxwSOxkjNzEzW}'

In this challenge, we had to change our directory to '/challenge/files' and then run '/challenge/run' with providing a single argument: a short (3 characters or less) globbed 
word with two '*' globs in it that covers every word that contains the letter p using '/challenge/run *p*'
```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{gyjBd098ta-9eenzfm7v5qcHeb1.0lM3kjNxwSOxkjNzEzW}
```

## What I Learned
I learnt that we can use multiple globs at a single time and how if we want to search for a single letter in a file we can use '*p*' to find it.
## References
None.
