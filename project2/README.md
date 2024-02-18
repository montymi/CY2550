# CY2550 Project 2

- [X] `project2/key.pub`
- [X]    RSA encryption
- [X]    4096 bits long
- [X]    Full name
- [X]    School email
- [X]    Profile picture
- [X]    Signature 1
- [X]    Signature 2
- [X] `project2/message.txt.asc`
- [X]    Encrypted with class key
- [X]    Signed by private key
- [X] Create [Keybase](https://keybase.io/) account
- [ ]    Follow Classmate 1
- [ ]    Follow Classmate 2
- [X] Add SSH key to [Github profile](https://github.com/montymi)

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
