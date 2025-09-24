# Catting Absolute Paths.
The challenge requires us to use the 'cat' command to read out files. In this case the flag for the challenge would be stored in a file called flag which we have to access using the entire absolute path.
As opposed to the previous challenge, here the path was provided in the terminal itself.
## My Solve
**Flag:** 'pwn.college{MLsR_sm0qd4O_1hoNXMHYm5ftRz.QXwITO0wSOxkjNzEzW}'

In this challenge, We simply had to use the 'cat' command to view the contents of the file 'flag' which was containing the flag we needed to pass the challenge but we had to provide the absolute patha as the argument.
As opposed to the previous challenge, here the path (/lib/python3.8/dbm/flag) was provided in the terminal itself.
```
hacker@commands~more-catting-practice:~$ cat /lib/python3.8/dbm/flag
pwn.college{MLsR_sm0qd4O_1hoNXMHYm5ftRz.QXwITO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can also use the 'cat' command by giving the argument as a absolute path of the file we want to read.
As opposed to the previous challenge, here the path was provided in the terminal itself.
## References
None.
