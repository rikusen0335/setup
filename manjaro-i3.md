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
