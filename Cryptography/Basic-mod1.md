## Description
We found this weird message being passed around on the servers, we think we have a working decryption scheme.
Download the message here.
Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.
Wrap your decrypted message in the picoCTF flag format (i.e. picoCTF{decrypted_message})

## Approach
What is Mod 37?
> To find 37 mod 37 using the Modulo Method, we first divide the Dividend (37) by the Divisor (37).
>  Second, we multiply the Whole part of the Quotient in the previous step by the Divisor (37).
>  Then finally, we subtract the answer in the second step from the Dividend (37) to get the answer. Here is the math to illustrate how to get 37 mod 37 using our Modulo Method:
>  37 ÷ 37 = 1
>  1 × 37 = 37
>  37 - 37 = 0
>  Thus, the answer to "What is 37 mod 37?" is 0.

Doing this manually is not a good solution so I wroe a Python script to do all these steps to decrypt this message.
![Screenshot from 2023-11-10 09-27-41](https://github.com/pixie-nukes/picoCTF/assets/94845416/58187cce-ba70-4920-99b9-31c1823b4aaa)

For the python script i referred to this [website](https://programmingfire.com/picoctf-2022-cryptography-basic-mod1)


## Output 
> picoCTF{R0UND_N_R0UND_79C18FB3}
