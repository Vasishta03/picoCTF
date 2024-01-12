## Problem
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm]

## Approach
After downoading the file and open it, I can see a PPT.
I extracted the power point presentation file to a zip file using [7zip](https://www.7-zip.org/). 
I was looking through the extracted files,I found the hidden file named as `ppt/slideMasters/hidden`
I read the file using the `cat` command. 
Reading that file `cat ppt/slideMasters/hidden`.
The output showed as follows `Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q` .
It showed a string of characters,in base64 format.
I then used [Base64](https://www.base64decode.org/) to convert the string into ASCII.
I got the flag,

## Output
The output after decoding using base 64 is flag: `picoCTF{D1d_u_kn0w_ppts_r_z1p5}`
