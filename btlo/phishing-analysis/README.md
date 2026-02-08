## [Phishing Analysis](https://blueteamlabs.online/home/challenge/phishing-analysis-f92ef500ce)
### Description
`A user has received a phishing email and forwarded it to the SOC. Can you investigate the email and attachment to collect useful artifacts?`  
  
**Tools:** Text Editor, Mozilla Thunderbird, URL2PNG, WHOis  
**Author:** BTLO      
**Difficulty:** Easy  

### Walkthrough
First, extract the provided file. You will receive a file with an `.eml` extension, which is an email file format. The first step is to open this file using an email client such as **Mozilla Thunderbird**, a commonly used email application on Linux.  
Once the email is opened, we can extract a large amount of information from this single piece of email evidence.  
  
![Email](images/email.png)  
  
The answers to **Question 1 to 3** can be found directly in the email headers shown above. Simply check the **Sent**, **To**, and **Subject** fields.  
  
**Question 1**  
>**Who is the primary recipient of this email?**  
<details><summary>Answer: </summary>kinnar1975@yahoo.co.uk</details>  
  
**Question 2**  
>**What is the subject of this email?**  
<details><summary>Answer: </summary>Undeliverable: Website contact form submission</details>  
  
**Question 3**  
>**What is the date and time the email was sent?**  
<details><summary>Answer: </summary>18 March 2021 04:14</details>  
  
**Question 4** is slightly more challenging for beginners, as it requires digging deeper into the email’s raw data. To do this, right-click on the email and select **View Page Source**. Then, use the find function (`Ctrl + F`) and search for the keyword **ip** to locate the originating IP address.  
  
![Page Source](images/page_source.png)  
  
**Question 4**  
>**What is the Originating IP?**  
<details><summary>Answer: </summary>103.9.171.10</details>  
  
Using the IP address identified in Question 4, we can now determine the resolved host by performing a reverse DNS lookup. This can be done using **whois.domaintools.com**.  
  
![Reverse DNS](images/reverse_dns.png)  
  
**Question 5**  
>**Perform reverse DNS on this IP address, what is the resolved host? (whois.domaintools.com)**  
<details><summary>Answer: </summary>c5s2-1e-syd.hosting-services.net.au</details>  
  
Next, return to the email view. At the bottom of the email, you can see an attachment. You can refer back to the first image for its location.  
  
**Question 6**  
>**What is the name of the attached file?**  
<details><summary>Answer: </summary>Website contact form submission.eml</details>  
  
Inspecting the contents of the attachment reveals a **suspicious URL** embedded within the email content.  
  
![Attachment Content](images/attachment.png)  

>[!NOTE]
>The URL below has been defanged. Please re-fang the URL in your answer. You may use CyberChef to do this.  

**Question 7**  
>**What is the URL found inside the attachment?**  
<details><summary>Answer: </summary>hxxps://35000usdperwwekpodf[.]blogspot[.]sg?p=9swghxxps://35000usdperwwekpodf[.]blogspot[.]co[.]il?o=0hnd</details>  
  
The hint for **Question 8** can be seen from the domain name in the URL. It points to a very popular free webpage hosting platform..  
  
**Question 8**  
>**What service is this webpage hosted on?**  
<details><summary>Answer: </summary>blogspot</details>  
  
To answer **Question 9**, submit the suspicious URL from Question 7 to the **URL2PNG** website. This tool generates a screenshot of the webpage, allowing you to view the page title even if the site is no longer accessible.  
  
![URL2PNG](images/url2png.png)  
  
**Question 9**  
>**Using URL2PNG, what is the heading text on this page? (Doesn't matter if the page has been taken down!)**  
<details><summary>Answer: </summary>Blog has been removed</details>  
