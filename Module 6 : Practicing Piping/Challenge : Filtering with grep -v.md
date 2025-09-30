# Filtering with grep -v
This challenge requires us to use 'grep' command with '-v' argument which basically shows all the options that do not match the entered value. 
## My Solve
**Flag:** 'pwn.college{0AlxijLJVnlqMWRGLeUeRj8yr0b.0FOxEzNxwSOxkjNzEzW}'

In this challenge, we simply had to use 'grep -v' which shows all the options that do not match the entered value (in this case : 'DECOY'). Here all the fake flags stored in
'/challenge/run' had the word 'DECOY' in them so we could filter out the original flag by using 'grep -v' and giving argument as 'DECOY
```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{0AlxijLJVnlqMWRGLeUeRj8yr0b.0FOxEzNxwSOxkjNzEzW}
```

## What I Learned
I learnt that 'grep' command with '-v' argument basically shows all the options that do not match the entered value exactly opposite to 'grep'.
## References
None.
