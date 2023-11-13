## Description
Download the disk image and use **mmls** on it to find the size of the Linux partition.
Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into **/tmp** not your home directory.

    Download disk image
    Access checker program: nc saturn.picoctf.net 64605

## Approach
I decompressed the file using the `gzip` command like this:
> `gzip -d disk.img.gz`

In this question we need to find the size of the disk. As hinted in the question let’s mmls

mmls - displays the contents of a volume system
> `mmls disk.img`

I connected to the server through netcat : `nc saturn.picoctf.net 64605`
And entered the size I got through mmls before. 

I got the flag!

## Output
picoCTF{mm15_f7w!}
