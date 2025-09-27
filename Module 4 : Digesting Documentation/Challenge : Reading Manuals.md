# Reading Manuals
The challenge requires us to use the 'man' command to display the manual of a command/program.
## My Solve
**Flag:** 'pwn.college{AplXa6Vuf4PPTWkWbx6n_JtJ14g.QX0EDO0wSOxkjNzEzW}'

In this challenge, a hint was hidden in the manual of 'challenge'. We had to use 'man challenge' to open the manual where it was specified that if we run the 
program '/challenge/challenge 'with argument '--plaufk 646' it will give us the required flag.
```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --plaufk 646
Correct usage! Your flag: pwn.college{AplXa6Vuf4PPTWkWbx6n_JtJ14g.QX0EDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'man' command to display the manual of any program/command. We need to specify the file name and not the file path, if we specify the file path 
as the argument we will see garbage being displayed as the man. To close the manual we simply press 'q'
## References
None.
