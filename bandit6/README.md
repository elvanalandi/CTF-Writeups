<h1>Bandit 6</h1>
SSH using password found in bandit5.

```
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

The next level password is stored on the server with the following properties:

```
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
```

Find the password using find command.

```
find / -user bandit7 -group bandit6 -size 33c -exec cat {} \; 2>/dev/null
```

To show the password, use cat command.
