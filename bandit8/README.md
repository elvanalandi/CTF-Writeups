<h1>Bandit 8</h1>
SSH using password found in bandit7.

```
ssh bandit8@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the file data.txt and is the only line of text that occurs only once. We can use the uniq and sort command to get the unique text that only occurs once.

```
cat data.txt | sort | uniq -u
```


