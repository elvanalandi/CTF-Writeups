<h1>Bandit 3</h1>
SSH using password from bandit2

```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

The next level password is stored in the hidden file in <strong>inhere</strong> directory. First, change the directory to the inhere directory.

```
cd inhere
```

Then, we reveal the hidden file using this command. This command also shows all the files in the directory.

```
ls -al
```

We can see that the hidden file is <strong>.hidden</strong>. The colour of the file is different from the others.

Get the password using cat command.

```
cat .hidden
```
