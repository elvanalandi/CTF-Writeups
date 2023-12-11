## Mod 26
### Description
`Cryptography can be easy, do you know what ROT13 is?`   
**Author:** PANDU  
**Flag Format:** picoCTF{FLAG}  
**Challenge Type:** Cryptography  
**Point:** 10 points  
**Ciphertext:** `cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_hyLicInt}`  

### Hints
<details><summary>1</summary>This can be solved online if you don't want to do it by hand!</details>

### Walkthrough
Based on the description, there is a hint—ROT13. A quick search on Google reveals that ROT13 is a straightforward letter substitution cipher, replacing each letter with the 13th letter after it in the Latin alphabet. Consequently, we can decrypt the ciphertext manually by substituting each letter with the corresponding one 13 positions later. Alternatively, numerous websites offer decryption tools, streamlining this process for us.

You may use the website that I used to decrypt it [here](https://www.dcode.fr/rot-13-cipher).

<details><summary>Flag</summary>picoCTF{next_time_I'll_try_2_rounds_of_rot13_ulYvpVag}</details>
