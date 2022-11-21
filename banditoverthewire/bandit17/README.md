<h1>Bandit 17</h1>
In this level, we must use the credentials that was retrieved in the previous level.
To use the credentials, we must change the permission of the file first.

```
chmod 400 bandit17.key
```

```
ssh bandit17@bandit.labs.overthewire.org -p 2220 -i bandit17.key
```

The next level password is stored in passwords.new and is the only line that has been changed between passwords.old and passwords.new.

We can differentiate the content of the two files using the command below.

```
diff passwords.new passwords.old
```


