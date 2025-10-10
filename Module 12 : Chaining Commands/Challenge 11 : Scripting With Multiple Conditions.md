## Scripting With Multiple Conditions
This challenge requires us to create a shell script and add if-elif-else conditional construct to it.
## My Solve
**Flag:** 'pwn.college{s32hs_y52zYX9cMkTqe7P8P33Lv.0FOzMDOxwSOxkjNzEzW}'

In this challenge, it was quite similar to the previous one, we just had to add 2 extra elif statements which would check for their respective conditions and then fall back 
upon the else statement.
```
hacker@chaining~scripting-with-multiple-conditions:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'if [ "$1" == "hack" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'then' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '     echo "the planet"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'elif [ "$1" == "pwn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'then' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '     echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'elif [ "$1" == "learn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'then' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '     echo "linux"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'else' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '     echo "unknown"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh
unknown
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{s32hs_y52zYX9cMkTqe7P8P33Lv.0FOzMDOxwSOxkjNzEzW}
```

## What I Learn
I learnt that we can also incorporate the elif statement with an if-else conditional construct, in the above mentioned format.
## References
None.
