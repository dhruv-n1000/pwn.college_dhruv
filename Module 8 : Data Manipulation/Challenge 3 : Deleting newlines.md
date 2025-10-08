# Deleting Newlines
This challenge requires us to use the 'tr -d' command to remove all the newline operators (\n)
## My Solve
**Flag:** 'pwn.college{0jFufDjy4gp70vO5Pp1T9F_DT44.0VNxEzNxwSOxkjNzEzW}'

In this challenge, we simply had to use 'tr -d' to remove the newline characters that initiated new lines in the data. 
We use ' /challenge/run | tr -d "\n" ' here to remove new lines
```
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{0jFufDjy4gp70vO5Pp1T9F_DT44.0VNxEzNxwSOxkjNzEzW}
```

## What I Learnt
we can use the delete 'tr -d' command to also remove any newline operator present in a piece of output by generalising all new lines under "\n".
## Reference
None.
