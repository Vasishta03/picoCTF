## Description
Files can always be changed in a secret way. Can you find the flag? **cat.jpg**

## Approach
I used **exiftool** to know the properties(details) of the image.
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/50d1404d-ddad-4ced-b54e-afbabb822cc2)
Then I converted the base64 text to ASCII text like this:
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/8da68e12-65bc-405d-bd87-170c9d6b4aca)

## Output
*picoCTF{the_m3tadata_1s_modified}*
