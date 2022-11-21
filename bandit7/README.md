<h1>Bandit 7</h1>
SSH using password found in bandit6.

```
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the file data.txt next to the word millionth. We can use cat and grep combination to get the password.

```
cat data.txt | grep millionth
```

