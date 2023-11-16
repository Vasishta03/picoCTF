## Description
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: **this**

## Approach
The challenge gives us a link to download an image named dolls.jpg. By the hint of the challenge, we know that there are hidden files in the image. So to extract the hidden files we use **binwalk**.
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/5005c762-c161-4016-b263-f19ed8120a37)
We see a directory named **base_images** that we head into and find another image file named **2_c.jpg**.
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/20e3dfdc-d5f8-4ee9-a75b-bd2edd775646)
We try binwalk again to extract any hidden files from this image as such and change our working directory to that of the extracted files.
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/c6dc85fc-0cbb-428c-b289-e6980856c048)
After many attempts, we get the flag.txt file. So we use cat tor ead the file.
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/27677cef-37aa-49da-a89b-695edfe0622d)

## Approach
**picoCTF{336cf6d51c9d9774fd37196c1d7320ff}**
