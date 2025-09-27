# Helpful Programs
The challenge requires us to know the alternatives of 'man'. In some cases manuals may not be available for every program,
in that case we use '--help' argument.
## My Solve
**Flag:** 'pwn.college{g_qoZuAHZKL2SBSluwDekXDwpVv.QX3IDO0wSOxkjNzEzW}'

In this challenge, we had to use '--help' argument along with '/challenge/challenge' command so that we get to open the help 
page. In that page we had many useful arguments which we could use. '-p' gave us a code(230) that we needed to enter with '-g'
argument so that the command '/challenge/challenge -g 230' gave us the flag.
```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 230
hacker@man~helpful-programs:~$ /challenge/challenge -g 238
Incorrect number! Look at the program help.
hacker@man~helpful-programs:~$ /challenge/challenge -g 230
Correct usage! Your flag: pwn.college{g_qoZuAHZKL2SBSluwDekXDwpVv.QX3IDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that whenever the 'man' command is not available we can use the '--help' argument along with the program path to 
display the help page. It contains several arguments we can use with the path of the program and their respective functions.
## References
None.
