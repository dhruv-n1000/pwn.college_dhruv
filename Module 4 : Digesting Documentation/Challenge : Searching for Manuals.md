# Searching For Manuals
The challenge requires us to dive a bit deeper into 'man' by hiding the manpage of challenge by replacing it with randomised name. We are required to use 'man man' and figure out things on our own from there.
## My Solve
**Flag:** 'pwn.college{kk6lMwbJ3cg8zePAhORQhFQQ9PR.QX2EDO0wSOxkjNzEzW}'

In this challenge, our man page of challenge was randomly renamed to anything, we had to open the 'man man' page and there we found out about 'man -k' searches for the entered
argument in short descriptions and files names. From there we found out taht we had to open man page of 'kklwbcgzeh' to find the flag. After that it showed us that we had to
run '/challenge/challenge' with a special argument : '--kklwbc 638' to get the flag'.
```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
i386 (8)             - change reported architecture in new program environment and/or set personality flags
ioctl_iflags (2)     - ioctl() operations for inode flags
kklwbcgzeh (1)       - print the flag!
linux32 (1)          - change reported architecture in new program environment and/or set personality flags
linux64 (1)          - change reported architecture in new program environment and/or set personality flags
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure ...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and confi...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure...
setarch (1)          - change reported architecture in new program environment and/or set personality flags
setarch (8)          - change reported architecture in new program environment and/or set personality flags
x86_64 (8)           - change reported architecture in new program environment and/or set personality flags
hacker@man~searching-for-manuals:~$ man kklwbcgzeh
hacker@man~searching-for-manuals:~$ /challenge/challenge --kklwbc 638
Correct usage! Your flag: pwn.college{kk6lMwbJ3cg8zePAhORQhFQQ9PR.QX2EDO0wSOxkjNzEzW}
```

## What I Learned
I learnt that we can use the 'man' command to learn about any command including 'man' itself. 'man -k flag' searches for flag in short descriptions and names. Then we can run
our normal file with special arguments to get different results.
## References
None.
