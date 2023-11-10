## Description
Can you find the flag in file? This would be really tedious to look through manually, something tells me there is a better way.

## Approach
I used the cat command to view the file, but it was:
![Screenshot from 2023-11-10 10-02-06](https://github.com/pixie-nukes/picoCTF/assets/94845416/e7a54894-378f-4c02-b1ad-7eb7b21d6138)

So i used the `grep` command to find and view the flag.
> cat file | grep picoCTF
I found the flag!

## Output
picoCTF{grep_is_good_to_find_things_dba08a45}
