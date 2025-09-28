# Multiple Options for Tab Completion
This challenge requires us to understand how the tab key works in case there are multiple options for tab key.
## My Solve
**Flag:** 'pwn.college{42KUqayKm5fuX5cvQZSQQKbYub7.0lN0EzNxwSOxkjNzEzW}'

In this challenge, we had to 'cd' to the directory '/challenge/files'. There, there were many files containing similar starting 
point to 'pwncollege-flag'. So we have to cut our way to the file by using tab completion multiple times.
```
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-f
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-fla
pwncollege-flag      pwncollege-flamingo
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-flag
pwn.college{42KUqayKm5fuX5cvQZSQQKbYub7.0lN0EzNxwSOxkjNzEzW}
```

## What I Learned
I learnt that if there are multiple cases possible for auto completion using tab, then using the tab key gives us a list of 
all possible comprehensions of the tab key and then we have to cut our way to the targeted file.
## References
None.
