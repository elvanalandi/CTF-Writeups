## [Secrets](https://blueteamlabs.online/home/challenge/secrets-85aa2bb3a9)  
### Description
`You’re a senior cyber security engineer and during your shift, we have intercepted/noticed a high privilege actions from unknown source that could be identified as malicious. We have got you the ticket that made these actions. You are the one who created the secret for these tickets. Please fix this and submit the low privilege ticket so we can make sure that you deserve this position.  
Here is the ticket:`  
**eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJmbGFnIjoiQlRMe180X0V5ZXN9IiwiaWF0Ijo5MDAwMDAwMCwibmFtZSI6IkdyZWF0RXhwIiwiYWRtaW4iOnRydWV9.jbkZHll_W17BOALT95JQ17glHBj9nY-oWhT1uiahtv8**  
**Tools:** CyberChef, hashcat   
**Author:** BTLO  
**Difficulty:** Easy  

### Walkthrough

![Base64](images/base64.png)  

**Question 1**  
>**Can you identify the name of the token? (Format: String)**  
<details><summary>Answer: </summary>JWT</details>

**Question 2**  
>**What is the structure of this token? (Format: Section.Section.Section)**  
<details><summary>Answer: </summary>Header, Payload, Signature</details>

**Question 3**  
>**What is the hint you found from this token? (Format: String)**  
<details><summary>Answer: </summary>_4_Eyes</details>

![Cracked JWT](images/cracked.png)  

**Question 4**  
>**What is the Secret? (Format: String)**  
<details><summary>Answer: </summary>bT!0</details>

![New Ticket](images/new-ticket.png)  

**Question 5**  
>**Can you generate a new verified signature ticket with a low privilege? (Format: String.String.String)**  
<details><summary>Answer: </summary>eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJmbGFnIjoiQlRMe180X0V5ZXN9IiwiaWF0Ijo5MDAwMDAwMCwibmFtZSI6IkdyZWF0RXhwIiwiYWRtaW4iOmZhbHNlfQ.nMXNFvttCvtDcpswOQA8u_LpURwv6ZrCJ-ftIXegtX4</details>
