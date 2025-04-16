## [Log Analysis - Privilege Escalation](https://blueteamlabs.online/home/challenge/log-analysis-privilege-escalation-65ffe8df12)  
### Description
`A server with sensitive data was accessed by an attacker and the files were posted on an underground forum. This data was only available to a privileged user, in this case the ‘root’ account. Responders say ‘www-data’ would be the logged in user if the server was remotely accessed, and this user doesn’t have access to the data. The developer stated that the server is hosting a PHP-based website and that proper filtering is in place to prevent php file uploads to gain malicious code execution. The bash history is provided to you but the recorded commands don’t appear to be related to the attack. Can you find what actually happened?`  
**Tools:** Text Editor  
**Author:** BTLO  
**Difficulty:** Easy  

### Walkthrough
**Question 1**  
>**What user (other than ‘root’) is present on the server?**  
<details><summary>Answer: </summary>daniel</details>

**Question 2**  
>**What script did the attacker try to download to the server?**  
<details><summary>Answer: </summary>linux-exploit-suggester.sh</details>

**Question 3**  
>**What packet analyzer tool did the attacker try to use?**  
<details><summary>Answer: </summary>tcpdump</details>

**Question 4**  
>**What file extension did the attacker use to bypass the file upload filter implemented by the developer?**  
<details><summary>Answer: </summary>.phtml</details>

**Question 5**  
>**Based on the commands run by the attacker before removing the php shell, what misconfiguration was exploited in the ‘python’ binary to gain root-level access? 1- Reverse Shell ; 2- File Upload ; 3- File Write ; 4- SUID ; 5- Library load**  
<details><summary>Answer: </summary>4</details>
