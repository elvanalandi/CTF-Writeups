<h1>Bandit 16</h1>
SSH using the previous level password.

```
ssh bandit16@bandit.labs.overthewire.org -p 2220
```

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000.

First, test the port using netcat command (port scanning).

```
nc -s -sv localhost 31000-32000
```

We have three available connection ports. The port that has the private key to the next level is 31790.
Then, we can submit the password to port 31790.

```
echo "cluFn7wTiGryunymYOu4RcffSxQluehd" | openssl s_client -connect localhost:31790 -ign_eof
```

Another way to implement port scanning is by using nmap tools.
