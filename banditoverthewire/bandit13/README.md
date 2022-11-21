<h1>Bandit 13</h1>
SSH using password found in bandit12.

```
ssh bandit13@bandit.labs.overthewire.org -p 2220
```

The next level can be accessed using private key to bandit14. However, there is a clue that the password for bandit15 is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14.

We can SSH to the bandit14 using our private key and localhost. 

```
ssh -i sshkey.private bandit14@localhost
```

See the password using cat command.

```
cat /etc/bandit_pass/bandit14
```
