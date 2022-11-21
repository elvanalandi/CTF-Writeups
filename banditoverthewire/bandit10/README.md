<h1>Bandit 10</h1>
SSH using password found in bandit9.

```
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the file data.txt, which contains base64 encoded data.

```
cat data.txt | base64 --decode
```
