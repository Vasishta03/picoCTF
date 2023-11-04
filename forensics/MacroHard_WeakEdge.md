## Problem
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm]

## Approach
I extracted the power point presentation file to a zip file using [7zip](https://www.7-zip.org/). I was looking through the extracted files, ppt/slideMasters/hidden looks suspicious.
Reading that file `cat ppt/slideMasters/hidden`.
Shows `Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q` .
I then used [Base64](https://www.base64decode.org/) to decode the file. 

## Output
The output after decoding using base 64 is flag: `picoCTF{D1d_u_kn0w_ppts_r_z1p5}`
