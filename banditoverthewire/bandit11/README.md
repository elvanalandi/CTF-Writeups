<h1>Bandit 11</h1>
SSH using password found in bandit10.

```
ssh bandit11@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions. To get the rotated characters, we can use the translate command (tr).

```
cat data.txt | tr [a-z][A-Z] [n-za-m][N-ZA-M]
```

