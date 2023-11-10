## Description
Sometimes you need to handle process data outside of a file.
Can you find a way to keep the output from this program and search for the flag? Connect to jupiter.challenges.picoctf.org 7480.

## Approach
I connected through netcat and using pipe and grep command i got the flag.
> nc jupiter.challenges.picoctf.org 7480 | grep picoCTF

## Output
picoCTF{digital_plumb3r_06e9d954}
