# Digital Ocean notes

## Fedora

```sh
# Package manager
dnf upgrade && dnf autoremove

# Once upon a time
dnf install \
    sudo \
    neovim git tmux curl wget rsync \
    htop fd-find bat ripgrep \
    go

# Enable wheel group
EDITOR=nvim visudo

# Add user
useradd -m -G wheel joker

# https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04
rsync --archive --chown=joker:joker ~/.ssh /home/joker

# Docker
# https://docs.docker.com/engine/install/fedora/

# https://github.com/haunt98/dotfiles
# https://gist.github.com/haunt98/97e006aa6f24aafef38d5b5164464723
# https://gist.github.com/haunt98/9eec914edfe3811e332c3959f958571d

# Redis
# https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-centos-8
# https://redis.io/topics/config
dnf install redis
nvim /etc/redis/redis.conf
systemctl enable --now redis.service
```
