# Translating Characters
This challenge requires us to use the 'tr' command to translate/modify the data.
## My Solve
**Flag:** 'pwn.college{w5u0OQqqrYukfZ1o4eNu9h4bSs2.01MxEzNxwSOxkjNzEzW}'

In this challenge, we simply had to use 'tr' to convert all the uppercase alphabets to lowercase alphabets and vice versa by adding the corresponding translated elements rightly.
```
hacker@data~translating-characters:~$ /challenge/run | tr ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
yOUR CASE-SWAPPED FLAG:
pwn.college{w5u0OQqqrYukfZ1o4eNu9h4bSs2.01MxEzNxwSOxkjNzEzW}
```

## What I Learnt
'tr' translates the character provided in its first argument to the character provided in its second argument. It can also handle multiple characters, with the characters in 
different positions of the first argument replaced with associated characters in the second argument.
## Reference
None.
