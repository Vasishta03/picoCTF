## Description
Can you figure out what is in the eax register at the end of the main function?
Put your answer in the picoCTF flag format: picoCTF{n} where n is the contents of the eax register in the decimal number base.
If the answer was 0x11 your flag would be picoCTF{17}. Disassemble this.

## Approach
> file debugger0_a
![Screenshot from 2023-11-10 08-39-01](https://github.com/pixie-nukes/picoCTF/assets/94845416/14a9e9ee-e71c-4a28-bb47-48756d1a7307)

Let’s begin by opening the downloaded file by passing it as an argument to GDB:
> gdb debugger0_a

for knowing more of the functions:
> info functions

The prime target here is the ‘main‘ function (address 0x1129).
Before proceeding, the gdb syntax is set to AT&T by default so i need to change it to intel which is more familliar to me.
> set disassembly-flavor intel
> disassemble main
![Screenshot from 2023-11-10 08-43-04](https://github.com/pixie-nukes/picoCTF/assets/94845416/e9eaf994-bbac-48aa-b174-3e8c6a74cba4)

I now found the eax registered value, so i used an python compiler to transform to hexadecimal value into a deimal, I did the following:
> print(int(0x86342))
Result: 549698


## Output
picoCTF{549698}
