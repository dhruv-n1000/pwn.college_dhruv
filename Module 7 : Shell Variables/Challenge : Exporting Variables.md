# Exporting Variables
This challenge requires us to use 'export' and export the variable so that it is available to all shell processes.
## My Solve
**Flag:** 'pwn.college{UIm86lqmnoIWicXLX8S7cKxXQ2S.QXyYTN0wSOxkjNzEzW}'

In this challenge, we simply had to use 'export' command on 'PWN' variable making it accessible to all shell processes.
```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{UIm86lqmnoIWicXLX8S7cKxXQ2S.QXyYTN0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can  use 'export' and export the variable so that it is available to all shell processes.
## References
None.
