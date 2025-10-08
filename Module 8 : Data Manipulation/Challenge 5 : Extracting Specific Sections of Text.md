# Extracting Specific Sections of Text
We are given a program with random numbers and a single character of the flag in a line, we are supposed to use cut to see a the specific column of characters and further 
pipe it into tr -d to remove newlines so we get the flag. 
## My Solve
**Flag:** 'pwn.college{4nxhCcuRARtHCPQkJAYVb0xEPUT.01NxEzNxwSOxkjNzEzW}'

I first ran the program /challenge/run to see which column contained the characters (2nd column seperated by a space), so I ran cut -d " " -f 2, which means that a space 
denotes different columns and that cut has to read the 2nd column, i then piped this output into tr -d '\n' which deleted the newlines. Hence, the single characters were \
combined to give me the flag. 
```
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{4nxhCcuRARtHCPQkJAYVb0xEPUT.01NxEzNxwSOxkjNzEzW}
```

## What I Learnt
I learnt how to use the cut program, how -d is used to specify the definition of a column and -f is used to specify the column number. 
## Reference
None.
