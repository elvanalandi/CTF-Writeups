<h1>Bandit 15</h1>
SSH using the previous level password.

```
ssh bandit15@bandit.labs.overthewire.org -p 2220
```

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

To do the SSL encryption connection, we can use openssl client.

```
echo "BfMYroe26WYalil77FoDi9qh59eK5xNr" | openssl s_client -connect localhost:30001 -ign_eof
```

-ign_eof is used for shutting down the connection when end of file is reached in the input.
