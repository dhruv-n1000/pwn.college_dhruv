## Scripting With Arguments
This challenge requires us to create a shell script with arguments.
## My Solve
**Flag:** 'pwn.college{cna8dWGKB8YgyvSk_74dd36k_Vi.0VNzMDOxwSOxkjNzEzW}'

In this challenge, we simply had to use 'echo' to write the commands into a shell script '/home/hacker/solve.sh'. Then we had to run it by using 'bash' command. But it should 
have a shebang and arugment usage.
```
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ echo 'echo "$2 $1"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ bash /home/hacker/solve.sh world hello
hello world
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{cna8dWGKB8YgyvSk_74dd36k_Vi.0VNzMDOxwSOxkjNzEzW}
```

## What I Learn
I learnt that we can accomodate arguments in shell scripts and pass them along with the shell script calling.
## References
None.
