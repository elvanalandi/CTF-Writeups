## Reaper
### Description
`Our SIEM alerted us to a suspicious logon event which needs to be looked at immediately . The alert details were that the IP Address and the Source Workstation name were a mismatch .You are provided a network capture and event logs from the surrounding time around the incident timeframe. Corelate the given evidence and report back to your SOC Manager.`   
**Author:** CyberJunkie  
**Difficulty:** Very Easy  

### Walkthrough
We will receive a zip file named **Reaper.zip**. Upon unzipping the file, I found a pcapng file and an evtx file.  

Let's move on to the first question: we need to find the IP address of Forela-Wkstn001. To do this, we can examine the nbns protocol in Wireshark. Open the pcapng file in Wireshark and apply a filter for the nbns protocol. You'll see the name of the workstation, which is **FORELA-WKSTN001**. NBNS (NetBIOS Name Service) works like DNS by translating names to IP addresses.  

![Wkstn001 IP Address](images/wkstn001.png)  

**Task 1**  
>Question: **What is the IP Address for Forela-Wkstn001?**  
<details><summary>Answer: </summary>172.17.79.129</details>  

Scroll down a bit, and you'll find the IP address for question 2.  

![Wkstn002 IP Address](images/wkstn002.png)  

**Task 2**  
>Question: **What is the IP Address for Forela-Wkstn002?**  
<details><summary>Answer: </summary>172.17.79.136</details>  

