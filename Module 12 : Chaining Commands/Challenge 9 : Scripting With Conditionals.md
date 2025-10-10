## Scripting With Conditional
This challenge requires us to create a shell script and include conditional statement in it.
## My Solve
**Flag:** 'pwn.college{Q34NeInZLZzcVR4gSzv8H7eFpRl.0lNzMDOxwSOxkjNzEzW}'

The challenge given to us is extremely similar to the example. I entered the lines of a simple conditional code to the shell script after adding the shebang. The conditional
was made such that the terminal will output 'college' if the bash recieves 'pwn' as the argument. I then used bash to run the shell script. This gave me the flag.
```
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'if [ "$1" == "pwn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'then' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo '     echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh japan
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{Q34NeInZLZzcVR4gSzv8H7eFpRl.0lNzMDOxwSOxkjNzEzW}
```

## What I Learn
I Learnt the syntax of conditional statements in linux shells and how they can be used.
## References
None.
