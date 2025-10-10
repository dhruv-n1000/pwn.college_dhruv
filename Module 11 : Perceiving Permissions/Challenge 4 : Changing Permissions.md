## Groups and Files
This challenge requires us to change the permissions of a file.

### Solve
**Flag:** 'pwn.college{stOqmY8s_yLpJKj1ORnkSdjyUM7.QXzcjM1wSOxkjNzEzW}'

We had to use the 'chmod' command to change the permissions of a particular file. Here we had to use the 'chmod' command to allow others to read the file '/flag' (o+r).
So that we as hacker can also read the file. Typically to use chmod on a file we must have the access to 'write' into that file but here its made an exception for learning 
purposes.
```
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{stOqmY8s_yLpJKj1ORnkSdjyUM7.QXzcjM1wSOxkjNzEzW}
```

### What I Learnt
I Learnt how we can change the permissions to a file.
When we use 'ls -l' in the star we get a long 10 character stringwhere : 
The first character there is the file type(file/directory). The next nine characters are the actual access permissions of the file or directory, split into 3 characters 
denoting permissions for the owning user (now you understand this!), 3 characters denoting the permissions for the owning group (now you understand this as well!), and 3 
characters denoting the permissions that all other access (e.g., by other users and other groups) has to the file.
IMPORTANT:
r - user/group/other can read the file (or list the directory)
w - user/group/other can modify the files (or create/delete files in the directory)
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
- - nothing 
For college_file above, the rw-r--r-- permissions entry decodes to:

r: the user that owns the file (user hacker) can read it
w: the user that owns the file (user hacker) can write to it
-: the user that owns the file (user hacker) cannot execute it
r: users in the group that owns the file (group hacker) can read it
-: users in the group that owns the file (group hacker) cannot write to it
-: users in the group that owns the file (group hacker) cannot execute it
r: all other users can read it
-: all other users cannot write to it
-: all other users cannot execute it
The basic usage for chmod is:

'chmod [OPTIONS] MODE FILE'
You can specify the MODE in two ways: as a modification of the existing permissions mode, or as a completely new mode to overwrite the old one.
In this level, we will cover the former: modifying an existing mode. chmod allows you to tweak permissions with the mode format of WHO+/-WHAT, where WHO is user/group/other
and WHAT is read/write/execute. For example, to add read access for the owning user, you would specify a mode of u+r. write and execute access for the group and the other
(or all the modes) are specified the same way. More examples:
->u+r, as above, adds read access to the user's permissions
->g+wx adds write and execute access to the group's permissions
->o-w removes write access for other users
->a-rwx removes all permissions for the user, group, and world
### References 
None. 
