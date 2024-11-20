Kali Linux custom configuration files.

## Installation

    sudo apt update -y
    sudo apt full-upgrade -y
    sudo apt install -y kali-linux-everything
    sudo apt install -y stow
    sudo apt install -y parallel
    sudo apt install -y ipcalc
    sudo apt install -y xclip
    sudo apt install -y alacritty
    sudo apt install -y bat
    mkdir -p ~/.local/bin
    ln -s /usr/bin/batcat ~/.local/bin/bat
    sudo apt install -y fd-find
    ln -s /usr/bin/fdfind ~/.local/bin/fd
    sudo apt install -y fzf
    sudo apt install -y ripgrep
    sudo apt install -y jq
    sudo apt install -y npm
    mkdir ~/.npm-global
    npm config set prefix '~/.npm-global'
    sudo apt install -y gcc-multilib
    sudo apt install -y g++-multilib
    sudo apt install -y mingw-w64
    sudo apt install -y musl-tools
    sudo apt install -y rustc
    sudo apt install -y autoconf
    sudo apt install -y automake
    sudo apt install -y autotools-dev
    mkdir ~/Code
    mkdir ~/Tools
    cp ~/.zshrc ~/.zshrc.bak
    curl -o ~/.vimrc -L https://raw.githubusercontent.com/devubu/vimrc/main/.vimrc
    mkdir -p ~/.vim/pack/themes/start
    git clone https://github.com/joshdick/onedark.vim.git ~/.vim/pack/themes/start/onedark.vim
    sudo cp ~/.vimrc /root/.vimrc
    sudo mkdir -p /root/.vim/pack/themes/start
    sudo git clone https://github.com/joshdick/onedark.vim.git /root/.vim/pack/themes/start/onedark.vim
    git clone https://github.com/devubu/.dotfiles.git ~/.dotfiles
    cd ~/.dotfiles
    stow .
    curl -o ~/Downloads/FiraCode.zip -L https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/FiraCode.zip
    unzip -q ~/Downloads/FiraCode.zip -d ~/Downloads/FiraCode -x "LICENSE" "readme.md" && rm ~/Downloads/FiraCode.zip
    sudo chown -R root:root ~/Downloads/FiraCode
    sudo mv ~/Downloads/FiraCode /usr/share/fonts/truetype
    fc-cache -f -v
    git clone https://github.com/tmux-plugins/tpm.git ~/.tmux/plugins/tpm
    ~/.tmux/plugins/tpm/bin/install_plugins
    curl -o ~/Downloads/nvim.appimage -L https://github.com/neovim/neovim/releases/download/v0.10.2/nvim.appimage
    sudo chown root:root ~/Downloads/nvim.appimage
    sudo chmod +x ~/Downloads/nvim.appimage
    sudo mv ~/Downloads/nvim.appimage /usr/bin/nvim
    nvim --headless "+q"
    source ~/.zshrc
