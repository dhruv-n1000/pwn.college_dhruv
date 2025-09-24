# Grepping For A Needle In A Haystack
The challenge requires us to use the 'grep' command to search for the content we need from the file. In this case the flag for the challenge would be stored in a file whose absolute path is /challenge/data.txt, but it would have 100s of lines of codes. We use the 'grep' command to find the flag.
## My Solve
**Flag:** 'pwn.college{U3xZ_WToE2zlmYojfO1rWeLuvNg.QX3EDO0wSOxkjNzEzW}'

In this challenge, We simply had to use the 'grep' command to search for the flag in a file whose absolute path is given and the file would have 100s of lines of text hence grepping would be necessary.
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{U3xZ_WToE2zlmYojfO1rWeLuvNg.QX3EDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'grep' command to search for particular content in a very large file and get all the lines containing that particular word/phrase in the entire file.
## References
None.
