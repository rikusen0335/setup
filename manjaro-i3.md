# Initial
```
yay -Syu
```

# Install applications
- Discord
- Alacritty
- Firefox
- Visual Studio Code
- ZSH
- tmux
- asdf-vm
- fcitx-mozc

```
yay -S discord alacritty firefox code zsh tmux fcitx-mozc fcitx-im fcitx-configtool adobe-source-han-sans-jp-fonts
```

### prezto
```
zsh

git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"

rm ~/.zshrc

setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done

chsh -s /bin/zsh
```

### asdf-vm
```
zsh

git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"

echo ". \$HOME/.asdf/asdf.sh" >> ~/.zshrc
```

# Edit config

### Alacritty
```
vim ~/.alacritty.yml
```
copy and paste this: https://github.com/alebelcor/alacritty-snazzy/blob/master/snazzy.yml

### fcitx

```vim ~/.xprofile

(paste these)

export LANG="ja_JP.UTF-8"
export XMODIFIERS="@im=fcitx"
export XMODIFIER="@im=fcitx"
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export DefaultIMModule=fcitx

vim ~/.zshrc

(paste these)

export GTK_IM_MODULE=fcitx
export XMODIFIERS=@im=fcitx
export QT_IM_MODULE=fcitx
```
