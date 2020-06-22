## initial
```
yay -Syu
```

### install applications
- Discord
- Alacritty
- Firefox
- Visual Studio Code
- ZSH
- tmux
- asdf-vm

```
yay -S discord alacritty firefox code zsh tmux
```

### asdf-vm
```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf
cd ~/.asdf
git checkout "$(git describe --abbrev=0 --tags)"

. $HOME/.asdf/asdf.sh
```
