# m0td
A simple bash script for printing useful MOTD

# Requirements:
lolcat
- Ubuntu: sudo apt install lolcat
- Arch: sudo pacman -S lolcat

figlet
- Ubuntu: sudo apt install figlet
- Arch: sudo pacman -S figlet

pfetch
- Ubuntu: build from source - git clone https://github.com/dylanaraps/pfetch
- Arch: yay -S pfetch

# Installation:
Just clone this repository and copy m0td to /usr/bin
```
$ git clone https://github.com/5412x/m0td
$ cd m0td
# chmod +x m0td
# cp m0td /usr/bin/
```

# Usage:
Then just run m0td whenever you want

For example, add m0td to your ~/.profile / ~/.bashrc / ~/.zshrc

Or add this so it runs only on connection via ssh
```
if [[ -n $SSH_CONNECTION ]] ; then
    m0td
fi
```
