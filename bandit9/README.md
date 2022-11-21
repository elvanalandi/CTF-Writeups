<h1>Bandit 9</h1>
SSH using password found in bandit8.

```
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters. We can use strings and grep command to get the password.

```
strings data.txt | grep -E "=+"
```

The grep -E command is used for regular expressions, and the strings command is used for printing the strings of printable characters in a file.
