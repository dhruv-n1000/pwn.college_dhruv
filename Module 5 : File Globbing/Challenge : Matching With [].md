# Matching with []
The challenge requires us to use a glab '[]'. When it encounters a '[]' character in any argument, the shell will treat it as a wildcard "single character" and try to replace
that argument with any any of the characters placed in '[]' if they are present in any files that match the pattern.
## My Solve
**Flag:** 'pwn.college{wL6puDsyBSRISFHTmnc0_UtzfdV.QXzIDO0wSOxkjNzEzW}'

In this challenge, we had to change our directory to '/challenge/files' and then run '/challenge/run' with a single argument that bracket-globs into file_b, file_a, file_s, 
and file_h using '/challenge/run file_[bash]'
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ ls
file_a  file_c  file_e  file_g  file_i  file_k  file_m  file_o  file_q  file_s  file_u  file_w  file_y
file_b  file_d  file_f  file_h  file_j  file_l  file_n  file_p  file_r  file_t  file_v  file_x  file_z
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{wL6puDsyBSRISFHTmnc0_UtzfdV.QXzIDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the glob '[]'. When it encounters a '[]' character in any argument, the shell will treat it as a single-character wildcard. This works like *, but only 
matches one character. Just that here the wildcard single character is limited to the characters provided in the '[]'
For instance : 
'cd /abc' can be written using '[]' as 'cd /a[b]c'
## References
None.
