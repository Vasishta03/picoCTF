## Description
What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this: **ciphertext**

## Approach
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/3f4f0cf9-3dc3-460a-85f2-77cce960ee11)


In RSA, `M**3` mod n = c. 
This can also be written as M**3 = tn + c for some t.
So, this means that M = iroot(tn+c, 3). 
I just need to find the right t. 
Given that (M ** 3) is only "barely" larger than n.
> I wrote a python code to decode the cipher text.

> ` sudo apt-get install -y python3-gmpy2` if you don't have gmpy2
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/08bc0c25-1290-48ef-ba4b-07fb07d2b112)

Found the Flag!

## Output
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/4d23ac27-c029-4b0c-b4b9-fff0d19a2fd3)
 **picoCTF{e_sh0u1d_b3_lArg3r_a166c1e3}**
