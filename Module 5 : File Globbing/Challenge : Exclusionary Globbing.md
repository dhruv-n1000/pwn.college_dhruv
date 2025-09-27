# Exclusionary Globbing
This challenge requires us to use '[]' in an exclusionary way, that is filter out the characters mentioned inside the '[]'
## My Solve
**Flag:** 'pwn.college{MyEpwtwAwUXig-5KR98oR9dOx9o.QX2IDO0wSOxkjNzEzW}'

In this challenge, we had to change our directory to '/challenge/files' and then run '/challenge/run' with all files that don't start 
with p, w, or n using '/challenge/run [!pwn]*'
```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ ls
amazing      delightful   great       jovial    magical     pwning   splendid   victorious  youthful
beautiful    educational  happy       kind      nice        queenly  thrilling  wonderful   zesty
challenging  fantastic    incredible  laughing  optimistic  radiant  uplifting  xenial
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{MyEpwtwAwUXig-5KR98oR9dOx9o.QX2IDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use glob '[]' to also allow all the single characters except those mentioned in the '[]' by using '!' before
mentioning the omitted characters.
## References
None.
