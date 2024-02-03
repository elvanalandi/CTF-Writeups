## [GrabThePhisher](https://cyberdefenders.org/blueteam-ctf-challenges/95/)
### Description
`An attacker compromised a server and impersonated https://pancakeswap.finance/, a decentralized exchange native to BNB Chain, to host a phishing kit at https://apankewk.soup.xyz/mainpage.php. The attacker set it as an open directory with the file name "pankewk.zip". Provided the phishing kit, you as a soc analyst are requested to analyze it and do your threat intel homework.`   
**Author:** Milann SHRESTHA     
**Difficulty:** Easy  

### Walkthrough
To initiate the lab, we must unzip the file named "c75-GrabThePhisher.zip," which has been provided, using the password: **cyberdefenders.org**.  
Initially, I explored the **index.html** file and identified various wallet options.    

**Q1**: **Which wallet is used for asking the seed phrase?**   
Notably, only one wallet's name matched the folder within the uncompressed directory.  
![Folder](images/folder.png)    

**Q2**: **What is the file name that has the code for the phishing kit?**   
Moving on to the next question, the file containing the code for the phishing kit is clearly noticeable. With the identification of a folder bearing the wallet's suspicious name, delving deeper into this folder will uncover a file sharing the same name, effectively addressing the second question.  

**Q3**: **In which language was the kit written?**  
The next question is straightforward; the file extension obtained from question 2 offers the solution to question 3.

**Q4**: **What service does the kit use to retrieve the victim's machine information?**   
For question 4, a deeper investigation into the file is necessary. On line 3, there is an API URL that appears suspicious. Accessing this URL in a browser reveals the victim's geolocation, indicating the service employed by the phishing kit to gather machine information.  

![Sypex Geo](images/geo.png)

**Q5**: **How many seed phrases were already collected?**   
Line 37 shows a function to write down something on a file. This could be a way for the attacker to collect the seed phrases. Inside the function, there is a path to the file.  

![Write Function](images/write.png)

Line 37 reveals a function for writing to a file, potentially a method for the attacker to gather seed phrases. Within this function, there is a specified file path. Therefore, inspecting the file path, starting from the root file (**pankewk**) and proceeding to **/log/log.txt**. We can count the line of the phrases to answer question 5.      

![Seed Phrases](images/phrases.png)  

**Q6**: **Write down the seed phrase of the most recent phishing incident?**   
To answer question 6, examine the last image and write down the final phrase.  

**Q7**: **Which medium had been used for credential dumping?**   
To identify the medium used for credential dumping, inspect the **sendTel**, which interacts with the Telegram API. This function indicates that Telegram is the chosen medium for credential dumping.  

![sendTel Function](images/sendTel.png)  

**Q8**: **What is the token for the channel?**   
The token for the Telegram channel is visible in the previous image, stored in a variable named **token**.

**Q9**: **What is the chat ID of the phisher's channel?**   
Likewise, the ID is found in the last image under a variable with the same name.

**Q10**: **What are the allies of the phish kit developer?**   
The next question is a bit different, but the answer is still in the same file. The phisher's allies left a message in the file, showing they are with the phisher using a nickname.  

![Message](images/message.png)  

**Q11**: **What is the full name of the Phish Actor?**   
The following question presents a challenge, requiring an understanding of Telegram API methods. You can see the methods from the documentation [here](https://core.telegram.org/bots/api#available-methods). A relevant method, such as the getChat method, can retrieve the Phish Actor's name. Formulating the URL as follows: `https://api.telegram.org/bot<Token>/getChat?chat_id=<Chat_ID>`. and inputting the token and chat ID, will get the information needed. The complete URL is provided below:  
`https://api.telegram.org/bot5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10/getChat?chat_id=5442785564`.  

The image below displays the response received from Telegram.  

![Telegram](images/telegram.png)

**Q12**: **What is the full name of the Phish Actor?**   
You can find the answer to the last question in the JSON response from Telegram, as shown in the image before.
