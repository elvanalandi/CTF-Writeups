<h1>Bandit 4</h1>
SSH using password found in bandit3.

```
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

The next password for bandit level 5 is in the only human-readable file in the <strong>inhere</strong> directory.

```
cd inhere
```

Check the files.

```
ls
```

Check the file format using file command.

```
file ./-file*
```

The human-readable file format is in ASCII text.

Get the password for the next level.

```
cat "./-file07"
```
