## Obedient Cat
### Description
`This file has a flag in plain sight (aka "in-the-clear").`   
**Author:** SYREAL  
**Flag Format:** picoCTF{FLAG}   
**Challenge Type:** General Skills
**Point:** 5 points

### Hints
<details><summary>1</summary>Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.</details>
<details><summary>2</summary>To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/0e428b2db9788d31189329bed089ce98/flag</details>
<details><summary>3</summary>$ man cat</details>

### Walkthrough
We can download the flag file through the link labeled Download flag, or alternatively, we can use the terminal command `wget https://mercury.picoctf.net/static/0e428b2db9788d31189329bed089ce98/flag` in the Terminal prompt. Once the file is downloaded, we can view its contents using the Linux `cat` command.

The contents of the file represent the flag for this challenge.
![Flag](flag.png)
