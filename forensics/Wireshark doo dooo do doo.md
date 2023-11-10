## Description
Can you find the flag? shark1.pcapng.

## Approach
I opened the file in wireskark. And typed in `tcp.stream eq 5` to get the 5th tcp stream.
Right click any entry, click `follow`, and then click `TCP Stream`.

The flag will now be shown, but it is encoded:
> Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}

So I used [ROT13](https://rot13.com/) to decode the flag and I found this 
> The flag is picoCTF{p33kab00_1_s33_u_deadbeef}

## Output
picoCTF{p33kab00_1_s33_u_deadbeef}
