## Nice Netcat
### Description
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 21135`, but it doesn't speak English...  
**Author:** SYREAL  
**Flag Format:** picoCTF{FLAG}   
**Challenge Type:** General Skills  
**Point:** 15 points

### Hints
<details><summary>1</summary>You can practice using netcat with this picoGym problem: <a href="https://play.picoctf.org/practice/challenge/34">what's a netcat?</a></details>
<details><summary>2</summary>You can practice reading and writing ASCII with this picoGym problem: <a href="https://play.picoctf.org/practice/challenge/22">Let's Warm Up</a></details>

### Walkthrough
In the description, there is a command that can be used to solve this challenge. When I run it in the command line, the output is a bunch of numbers. It looks like codes, but what kind of code is that? One of the hints showed the clue to the codes. The numbers represent ASCII codes. 

![Netcat](nc.png)

Therefore, we must convert it to a text-readable string to reveal the truth behind it. I used an online [ASCII-to-text converter](https://codebeautify.org/ascii-to-text) to simplify the process rather than decoding it one by one. Then, the flag revealed itself 😀.

![Flag](flag.png)
