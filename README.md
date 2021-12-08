# Digital Ocean notes

## Fedora

```sh
# Suppose you are root, first install something then create a new user

# Package manager
dnf upgrade && dnf autoremove

# Once upon a time
dnf install sudo

# Enable wheel group
EDITOR=nvim visudo

# Add user
useradd -m -G wheel joker

# https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04
rsync --archive --chown=joker:joker ~/.ssh /home/joker

# Docker
# https://docs.docker.com/engine/install/fedora/

# https://github.com/haunt98/dotfiles
# https://gist.github.com/haunt98/9eec914edfe3811e332c3959f958571d
```
