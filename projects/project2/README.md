# CY2550 Project 2

[ ] `project2/key.pub`
\t[X] RSA encryption
\t[X] 4096 bits long
\t[X] Full name
\t[X] School email
\t[X] Profile picture
\t[ ] Signature 1
\t[ ] Signature 2
[X] `project2/message.txt.asc`
\t[X] Encrypted with class key
\t[X] Signed by private key
[X] Create [Keybase](https://keybase.io/) account
[ ] Follow Classmate 1
[ ] Follow Classmate 2
[X] Add SSH key to Github profile

## Signing a Public Key
```
#!/bin/bash

# IMPORTING #
cd $(mktemp -d)
git clone git@github.com:montymi/CY2550.git  # {OR} https `git clone https://github.com/montymi/CY2550.git`
cd CY2550
gpg --import "./projects/project2/key.pub"

# SIGNING #
gpg --sign-key montanaro.m@northeastern.edu

# EXPORTING #
git checkout project2
gpg --armor --export montanaro.m@northeastern.edu > NAME_signed_key.pub
git add .
git commit -m "signed"
git push
```

## Following User on Keybase
```
keybase follow USERNAME_HERE
```
