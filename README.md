# Digital Ocean notes

## Fedora

```sh
# Package manager
dnf upgrade && dnf autoremove

# Once upon a time
dnf install \
    sudo \
    neovim git tmux curl wget rsync \
    rust-fd-find rust-bat ripgrep \
    go

# Enable wheel group
EDITOR=nvim visudo

# Add user
systemctl enable --now systemd-homed.service
homectl create joker --member-of=wheel

# https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04
rsync --archive --chown=joker:joker ~/.ssh /home/joker

# Docker
# https://docs.docker.com/engine/install/fedora/

# https://github.com/haunt98/dotfiles
# https://gist.github.com/haunt98/97e006aa6f24aafef38d5b5164464723
# https://gist.github.com/haunt98/9eec914edfe3811e332c3959f958571d
```
