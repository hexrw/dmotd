# m0td
A simple bash script for printing useful MOTD
Btw it's with zero not with o

# Requirements:
lolcat
- Ubuntu: `sudo apt install lolcat`
- Arch: `sudo pacman -S lolcat`

figlet
- Ubuntu: sudo apt install figlet
- Arch: `sudo pacman -S figlet`

pfetch
- Ubuntu: build from source - `git clone https://github.com/dylanaraps/pfetch`
- Arch: `yay -S pfetch` or build from source (same as above)

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

For example, add `m0td` to your ~/.profile

Or add this so it runs only on connection via ssh
```
if [[ -n $SSH_CONNECTION ]] ; then
    m0td
fi
```

You may also want to disable default SSH motd, this usually works
```
$ touch ~/.hushlogin
# chmod -x /etc/update-motd.d/*
```
editing /etc/motd is also sometimes a solution

# Example:
![example command output](https://github.com/5412x/m0td/blob/main/example.png?raw=true)
