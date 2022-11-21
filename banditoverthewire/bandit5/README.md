<h1>Bandit 5</h1>
SSH using password found in bandit4.

```
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the <strong>inhere</strong> directory with the following properties:

```
- human-readable
- 1033 bytes in size
- not executable
```

First, change the directory to the <strong>inhere</strong> directory.

```
cd inhere
```

Then, find the file using find command.

```
find . -type f -size 1033 ! -executable -exec file {} + | grep ASCII
```
