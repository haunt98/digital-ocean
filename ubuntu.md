# Ubuntu

```sh
apt update && apt upgrade -y && apt autoremove -y && apt autoclean

# Increase swap
fallocate -l 8G /swapfile
chmod 600 /swapfile
mkswap /swapfile
swapon /swapfile

cp /etc/fstab /etc/fstab.bak
echo '/swapfile none swap sw 0 0' | tee -a /etc/fstab

# Essential
apt install -y \
    build-essential \
    git \
    tmux \
    rsync

# Docker
apt install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -

add-apt-repository -y \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

apt install -y docker-ce docker-ce-cli containerd.io docker-compose

# Neovim
add-apt-repository -y ppa:neovim-ppa/stable
apt install -y neovim

# Dotfiles
git clone --depth=1 https://github.com/haunt98/dotfiles.git
cd ~/dotfiles
./install.sh
```

`~/.bashrc`:

```bash
export HISTIGNORE="cd:ls:la:ll:pwd:exit"

[[ -f /usr/share/bash-completion/bash_completion ]] && \
    source /usr/share/bash-completion/bash_completion

export EDITOR=nvim
[[ -f /usr/bin/nvim ]] && \
    alias vim="nvim"
```
