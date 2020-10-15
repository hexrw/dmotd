# m0td
A simple bash script for printing useful MOTD

Btw it's with zero not with o
 
![m0td's logo](https://github.com/5412x/m0td/blob/main/logo.png?raw=true)

# Recommended (not strictly required but...):
lolcat - make it colorful - you can use it for anything by piping input to it (like `ls | lolcat`)
- Ubuntu: `sudo apt install lolcat`
- Arch: `sudo pacman -S lolcat`

figlet - prints big IP - you also can use it for anything by piping input to it
- Ubuntu: sudo apt install figlet
- Arch: `sudo pacman -S figlet`

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
Valid arguments are `-h` or `--help` and `-v` or `--version`

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
