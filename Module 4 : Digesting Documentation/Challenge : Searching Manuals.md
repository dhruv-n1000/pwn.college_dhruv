# Searching Manuals
The challenge requires us to use the '/' to search a particular thing in a manual being displayed.
## My Solve
**Flag:** 'pwn.college{UOiisr9cDM-eZwOM2iVmpDV1ak3.QX1EDO0wSOxkjNzEzW}'

In this challenge, We initially had to open manual of challenge, where the content was too much, hence we had to use '/' to search for the flag.
There were many arguments that were neat bbut did not yield the flag, only '-j' yielded the flag which I found out using '/' and then repeatedly using 'n'
to go for the next result.
```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge -j
Initializing...
Correct usage! Your flag: pwn.college{UOiisr9cDM-eZwOM2iVmpDV1ak3.QX1EDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use '/' to find a particular result in a manual being displayed. We can use 'n' to go to the next result, 'N' to go the the previous result and '?' to 
search for the required result backwards.
## References
None.
