## Description
We found this file. Recover the flag.

## Approach
I opened the file in [hexed](hexed.it) and understoof that it was a **bmp** file.
Since I was using the debian distro, I can easily findout using my normal image viewer as a bmp file. 
![Screenshot from 2023-11-12 11-03-35](https://github.com/pixie-nukes/picoCTF/assets/94845416/60bc3887-3e69-4d55-a567-298682b56699)

I downloaded a sample bmp image from the web and compared it with the file given in [hexed](hexed.it) as shown below.
![Screenshot from 2023-11-12 11-26-23](https://github.com/pixie-nukes/picoCTF/assets/94845416/1971b2ba-ebca-4054-878b-eb003dc62e31)
![Screenshot from 2023-11-12 11-26-41](https://github.com/pixie-nukes/picoCTF/assets/94845416/54ab5f64-c528-4726-94ec-8109b30c31ad)
I found some discrepencies and corrected the size in the first row. and i downloaded the image.
![Screenshot from 2023-11-12 11-27-54](https://github.com/pixie-nukes/picoCTF/assets/94845416/c1e157c4-a71e-4277-ad33-501351315b5d)
But the problem was that the image was only half and the height was not upto its fullest length. 

So I used the **exiftool** to get the image properties
![Screenshot from 2023-11-12 11-29-56](https://github.com/pixie-nukes/picoCTF/assets/94845416/703757bf-544c-4f47-84c3-ecc462718ce0)

So I used python compiler to convert the image height and image width to hex format to view and change in [hexed](hexed.it).
![image](https://github.com/pixie-nukes/picoCTF/assets/94845416/a353816c-2fc8-4239-84a1-0d7030594c81)
![Screenshot from 2023-11-12 11-32-12](https://github.com/pixie-nukes/picoCTF/assets/94845416/a5c39256-bf47-4258-ae9b-3327ef1f1d15)
![Screenshot from 2023-11-12 11-33-39](https://github.com/pixie-nukes/picoCTF/assets/94845416/32852ad7-955c-4059-b6f4-c96094284e68)
The image height is different but the image width is same. so i need to change the image height.
I searched on google the maximum permitted height for a bmp file.
![Screenshot from 2023-11-12 11-34-58](https://github.com/pixie-nukes/picoCTF/assets/94845416/f305890a-83fd-4645-8b59-214b6f628c2d)
And i converted the same in [hexed](hexed.it)
I downloaded the new image, in which i recovered the flag. 
![Screenshot from 2023-11-12 11-36-35](https://github.com/pixie-nukes/picoCTF/assets/94845416/450c7c50-3458-4ba9-afd1-021ca761267b)

## Output
picoCTF{qu1t3_a_v13w_2020}
