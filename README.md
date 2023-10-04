# Delightful Message Of The Day (DMOTD)

DMOTD is a simple Bash script designed to enhance the appearance of your Message of the Day (MOTD). It provides a visually appealing replacement for the default MOTD.

![Logo](https://github.com/hexrw/dmotd/blob/main/logo.png?raw=true)

## Optional Dependencies

1. **lolcat**: Colors the output
    - Versions confirmed to be compatible are _v1.3_ and _v1.4_.
    - Ubuntu: `sudo snap install lolcat` - Don't install from the APT repository as it often contains an outdated version of `lolcat` that might be incompatible with this script.
    - Arch: `sudo pacman -S lolcat`

3. **figlet**: ASCII fonts
    - The only version confirmed to be compatible is __v2.2.5__.
    - Ubuntu: `sudo apt install figlet`
    - Arch: `sudo pacman -S figlet`

## Installation

As straightforward as cloning the `dmotd` script from this repository.

### Example installation using Wget

```sh
# All users
# Downloads the script from GitHub into `/usr/local/bin/dmotd` and then gives the execute permission
wget -O /usr/local/bin/dmotd "https://github.com/hexrw/dmotd/blob/main/dmotd?raw=true" && sudo chmod +x /usr/local/bin/dmotd
```

```sh
# Current user only (make sure `~/.local/bin` is in PATH)
# Downloads the script from GitHub into `~/.local/bin/dmotd` and then gives the execute permission
wget -O ~/.local/bin/dmotd "https://github.com/hexrw/dmotd/blob/main/dmotd?raw=true" && sudo chmod +x ~/.local/bin/dmotd
```

## Usage

Valid arguments are `-h` or `--help` and `-v` or `--version`

### Example Usage

#### Disable the default MOTD

```sh
# Works for most distributions
# You can also try to disable it by editing /etc/motd
touch ~/.hushlogin
sudo chmod -x /etc/update-motd.d/*
```

#### Run `dmotd` on login

Add

```sh
dmotd
```

OR

```sh
# For SSH only
if [[ -n $SSH_CONNECTION ]] ; then
    dmotd
fi
```

to `~/.bashrc` (if you use BASH as your default shell)

## Examples

![Example Output](https://github.com/5412x/m0td/blob/main/example.png?raw=true)
