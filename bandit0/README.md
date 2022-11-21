<h1>Bandit 0</h1>
<p>We are given SSH URL, username, password, and port number to connect to the CTF.</p>
<p>The next step is SSH with the given credentials</p>

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
Then, input the given password.

Get the level 1 password in the home directory by using cat command.

```
cat ./~
```

The flag will be shown to us, which is the password itself.

