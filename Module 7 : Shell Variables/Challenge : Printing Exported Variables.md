# Printing Exported Variables
This challenge requires us to use 'env' command which prints every exported variable set in the shell.
## My Solve
**Flag:** 'pwn.college{oNpl6adb_O8ZQwb55INH6oZ5YZH.QX4UTN0wSOxkjNzEzW}'

In this challenge, we simply had to use 'env' command to print every exported variable set in the shell one of which includes
the flag itself.
```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=ab1060798b97a3a10a24f9286281cfc48412e9f52ea06dcf335e7bb65f9cb8cb
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{oNpl6adb_O8ZQwb55INH6oZ5YZH.QX4UTN0wSOxkjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I Learn
I learnt that we can use 'env' command to print every exported variable set in the shell.
## References
None.
