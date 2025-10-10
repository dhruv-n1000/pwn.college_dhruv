## Scripting with default cases
This challenge requires us to create a shell script and add if-else conditional construct to it. 
## My Solve
**Flag:** 'pwn.college{4B36i8uxTdfvr-bLT2wSindmu0r.01NzMDOxwSOxkjNzEzW}'

In this challenge, it was quite similar to the previous one, we just had to add an extra else statement which would print 'nope' if any other value apart from 'pwn' was entered
as an argument.
```
hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'if [ "$1" == "pwn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'then' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo '     echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'else' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo '     echo "nope"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ chmod ugo+x /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ /home/hacker/solve.sh
nope
hacker@chaining~scripting-with-default-cases:~$ /home/hacker/solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{4B36i8uxTdfvr-bLT2wSindmu0r.01NzMDOxwSOxkjNzEzW}
```

## What I Learnt
I learnt that we can also incorporate the else statement with an if statement using the above mentioned format.
## References
None.
