<h1>Bandit 14</h1>
SSH using password found in /etc/bandit_pass/bandit14.

```
ssh bandit14@bandit.labs.overthewire.org -p 2220
```

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost. To retrieve the password, we can use netcat and echo command.

```
echo "4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e" | nc 127.0.0.1 30000
```

127.0.0.1 is the same as localhost, and 30000 is the port number. Echo command is used to submit the password.
