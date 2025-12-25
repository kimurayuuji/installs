# tmux

## repository

https://github.com/tmux/tmux

## my config

https://github.com/kimurayuuji/tmux

## my .bashrc

```bash
## 初回シェル時のみ tmux実行
if [ $SHLVL = 1 ]; then
  tmux
fi
```

# eza

## repository

https://github.com/eza-community/eza

## my .bashrc

```bash
alias ls='eza --icons=always --color=always'
alias la='ls -la'
alias lat4='ls -laT -L=4'
alias lat2='ls -laT -L=2'
alias lt4='ls -lT -L=4'
alias lt2='ls -lT -L=2'
```

# bat

## repository

https://github.com/sharkdp/bat


## my .bashrc

```bash
alias bat="batcat"
```

# fzf

## repository

https://github.com/junegunn/fzf

## my .bashrc

```bash
[ -f ~/.fzf.bash ] && source ~/.fzf.bash
```

# zoxide

## repository

https://github.com/ajeetdsouza/zoxide

## my .bashrc

```bash
eval "$(zoxide init bash)"
```

# yazi

## repository

https://github.com/sxyazi/yazi

## my config

https://github.com/kimurayuuji/yazi


## my .bashrc

```bash
export EDITOR=nvim

function y() {
  zoxide add $(pwd)
  local tmp="$(mktemp -t "yazi-cwd.XXXXXX")" cwd
  yazi "$@" --cwd-file="$tmp"
  if cwd="$(command cat -- "$tmp")" && [ -n "$cwd" ] && [ "$cwd" != "$PWD" ]; then
    builtin cd -- "$cwd"
    zoxide add "$cwd"
  fi
  rm -f -- "$tmp"
}
```


# neovim

## repository

https://github.com/neovim/neovim

## my AstroNvim

https://github.com/kimurayuuji/astrovim-template


# lazygit

## repository

https://github.com/jesseduffield/lazygit


# lazydocker

## repository

https://github.com/jesseduffield/lazydocker


# glow

## repository

https://github.com/charmbracelet/glow

# ripgrep

## repository

https://github.com/BurntSushi/ripgrep

# rclone

## repository

https://github.com/rclone/rclone

## how to set up for google drive

https://qiita.com/devzooiiooz/items/f08c7bb9e935a79f7367


# zsh-autocomplete

## repository 

https://github.com/marlonrichert/zsh-autocomplete

## my .bashrc

```bash
# source {zsh-autocomplete clone}/zsh-autocomplete.plugin.zsh
source /home/kimurayuuji/git/zsh-autocomplete/zsh-autocomplete.plugin.zsh
```


# nb

## repository

https://github.com/xwmx/nb

## completion

```bash
sudo nb completions install --download
```

