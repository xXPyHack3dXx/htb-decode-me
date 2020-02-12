# Decode Me
Solution to Hack The Box Challenge - Decode Me

### Problem

Try find the flag!

### Solution

There are two strings both of them ends with "=" so probably is related to Base64, but no...
Due to the breakline its appears to be a key and the string to decrypt but with what algorithm?

Its fernet cipher by experience [(ref)](https://github.com/xXPyHack3dXx/htb-keys). Decrypting...

```bash
RCdgTl45OFs8O3tGMlZVNTRRPythcUw6bVxJNmlYJmYkMEBSeFBfdSldeHFwdW5tM3Fwb2htZmUrTGJnZl9eXSNhYFleV1Z6VFNYUVZVTnJMUVBPTkdrS0QsSEFlKERDPDtfPz5+fTVZOTg3dzUuUjJyMC8oJyZKKikoJyYlfHtBeX53djx6eXhxWTZ0c1VUcG9oLnk=
```

That is a Base64 string. Decrypting with [tool](https://www.base64decode.org/)

```bash
D'`N^98[<;{F2VU54Q?+aqL:m\I6iX&f$0@RxP_u)]xqpunm3qpohmfe+Lbgf_^]#a`Y^WVzTSXQVUNrLQPONGkKD,HAe(DC<;_?>~}5Y987w5.R2r0/('&J*)('&%|{Ay~wv<zyxqY6tsUTpoh.y
```

**WTF???**

Searching in the forum found that the challenge was related to another HTB challenge "inferno" that was related to Dante's inferno because in some part it uses a programming language which name is the same that a level in the game. The level/language name is **Malbolge** and using this [tool](http://malbolge.doleczek.pl/) you get the flag
