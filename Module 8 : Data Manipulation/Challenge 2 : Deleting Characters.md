# Deleting Characters
This challenge requires us to use the 'tr' command to translate the data mentioned into nothing (which basically means deleting it)
## My Solve
**Flag:** 'pwn.college{UOqSp_qbPsQFNBoInhLQh2HZ7AI.0FNxEzNxwSOxkjNzEzW}'

In this challenge, we simply had to use 'tr' to translate the data mentioned into nothing meaning we had to delete '^' and '%', as it was unnecessarily included in the flag.
```
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{UOqSp_qbPsQFNBoInhLQh2HZ7AI.0FNxEzNxwSOxkjNzEzW}
```

## What I Learnt
'tr' can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete.
## Reference
None.
