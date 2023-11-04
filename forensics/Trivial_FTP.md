## Problem
Figure out how they moved the [flag].

## Approach
- I opened the packet using wireshark. `file > export objects > tftp` and i downloaded all the files.
- I opened the `instructions` document to find `GSGCQBRFAGRAPELCGBHEGENSSVPFBJRZHFGQVFTHVFRBHESYNTGENAFSRE.SVTHERBHGNJNLGBUVQRGURSYNTNAQVJVYYPURPXONPXSBEGURCYNA`
I copied this tect and put it into [Rot13](rot13.com) and got the output as `TFTPDOESNTENCRYPTOURTRAFFICSOWEMUSTDISGUISEOURFLAGTRANSFER.FIGUREOUTAWAYTOHIDETHEFLAGANDIWILLCHECKBACKFORTHEPLAN`.
It didnt make any sense so i tried to read it with spaces and i found this `t ftp doesnt encrypt our traffic so we must disguise our flag transfer figure out away to hide the flag and i will check back for the plan`.
- I opened the `plan` document to find `VHFRQGURCEBTENZNAQUVQVGJVGU-QHRQVYVTRAPR.PURPXBHGGURCUBGBF` and again i used ROT13 decoder to decode and i found out with spaces as `i used the program and hid it with due diligence check out the photos`.
- I extracted the `program.deb` file and found that it was a `steghide` using the command `sudo dpkg -i program.deb`.
- The hint from the plan document suggests that `DUEDILIGENCE` (uppercase because the encoded text is uppercase) is the password.
- I used `steghide` on every image included in the packet capture file.
  The flag is hidden in the last image `picture3.bmp`. So I ran `steghide extract -sf picture3.bmp -p DUEDILIGENCE` and `cat flag.txt` to get the flag.

  ## Output
  picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}
