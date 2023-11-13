## Description
We found a brand new type of encryption, can you break the secret code? (Wrap with picoCTF{})
**kjlijdliljhdjdhfkfkhhjkkhhkihlhnhghekfhmhjhkhfhekfkkkjkghghjhlhghmhhhfkikfkfhm** **new_caesar.py**

## Approach
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/65ffee58-d9cf-4b46-b871-9f3b4d813129)

1. The assert statements show that the key needs to be one character and be a letter between a to p.
2. Using enumerate loops through the values of b16, assigning i to the index at a particular point and c the value.
3. The function shift returns a value in ALPHABET at the index ascii value of the c minus 97 plus the ascii value of the key minus 97 mod 16.

I edited the code a bit like this and applie dthe cipher text like this:
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/ece5a059-d615-46c0-8f12-7c97834cd81f)

After running the code, I got this:
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/7a8de320-fc5c-4f67-9175-7ca0fad2b020)


## Output
**picoCTF{et_tu?_1ac5f3d7920a85610afeb2572831daa8}**
