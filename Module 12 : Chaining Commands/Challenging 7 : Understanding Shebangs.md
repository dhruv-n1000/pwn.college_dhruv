## Understanding Shebangs
This challenge requires us to make a shell script with the correct Shebang which outputs 'hack the planet'. After this, on running /challenge/run, we will get the flag
## My Solve
**Flag:** 'pwn.college{0VvMysTckPNWCPhYwvL_G8xdIIt.0VOzMDOxwSOxkjNzEzW}'

In this challenge we first created the shell script with the shebang as bash and then appended the echo command to it. We then altered the permissions for the shell script so it 
could be explicitly run without bash. On running /challenge/run, it verified the challenge and gave us the flag.
```
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ echo 'echo "hack the planet"' >> /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ chmod u+xwr /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{0VvMysTckPNWCPhYwvL_G8xdIIt.0VOzMDOxwSOxkjNzEzW}
```

## What I Learn
I learnt that shebangs are the first characters at the start of a script which tells the operating system which interpreter to use.

## References
None.
