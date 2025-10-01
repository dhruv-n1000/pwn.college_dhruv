# Reading Input
This challenge requires us to use 'read' command to allow us to enter an input into any particular variable.
## My Solve
**Flag:** 'pwn.college{wNG6pfVLHunEKKtG1y7yiqyqWPz.QX4cTN0wSOxkjNzEzW}'

In this challenge, we simply had to use 'read' command on 'PWN' variable and then entering input value to assign it to 'PWN'.
```
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{wNG6pfVLHunEKKtG1y7yiqyqWPz.QX4cTN0wSOxkjNzEzW}
```

## What I Learn
I learnt that we can  use 'read' command to allow us to enter an input into any particular variable. Using the argument '-p', we can enter a prompt in the terminal prompting
the user to enter some value.
eg : 
hacker@dojo:~$ read -p "INPUT: " MY_VARIABLE
INPUT: Hello!
hacker@dojo:~$ echo "You entered: $MY_VARIABLE"
You entered: Hello!
## References
None.
