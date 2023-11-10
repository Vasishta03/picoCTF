## Description
What integer does this program print with arguments 182476535 and 3742084308? 

File: `chall.S` Flag format: picoCTF{XXXXXXXX} -> (hex, lowercase, no 0x, and 32 bits. ex. 5614267 would be picoCTF{0055aabb})

## References
I used this sites to know about how arm assembly works
1. [Instruction Set](https://azeria-labs.com/arm-instruction-set-part-3/)
2. [Architecture](https://developer.arm.com/documentation/ddi0487/latest)

I used the below site to learn how to cross compile ARM assembly on x86
1. [ARMv8 via Command Line](https://github.com/joebobmiles/ARMv8ViaLinuxCommandline)

## Approach
Installing a Cross Compiler
> `$ sudo apt install binutils-aarch64-linux-gnu`

Compiling ARMv8
> `aarch64-linux-gnu-as -o chall.o chall.S`
> `aarch64-linux-gnu-gcc -static -o chall chall.o`

I need to install a version of QEMU that runs statically in the background with `sudo apt install qemu-user-static` so I can run ARM binaries like normal programs.

Finally, I can run the challenge binary with the two provided arguments: `./chall 182476535 3742084308`

>Result: 3742084308

The flag format should be in hexadecimal according to the question so I can use a hexadecimal convertor like [Rapid Tables](https://www.rapidtables.com/convert/number/decimal-to-hex.html)

>Result: df0bacd4

## Output
Flag format: picoCTF{XXXXXXXX} -> (hex, lowercase, no 0x, and 32 bits
So,
>picoCTF{df0bacd4}
