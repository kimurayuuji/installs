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

## version

```
tmux -V
tmux next-3.7
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

## version

```
eza -v
eza - A modern, maintained replacement for ls
v0.23.4 [+git]
https://github.com/eza-community/eza
```

# bat

## repository

https://github.com/sharkdp/bat


## my .bashrc

```bash
alias bat="batcat"
```

## version

```
batcat --version
bat 0.24.0
```

# fzf

## repository

https://github.com/junegunn/fzf

## my .bashrc

```bash
[ -f ~/.fzf.bash ] && source ~/.fzf.bash
```

## version
```
fzf --version
0.70.0 (eacef5ea)
```

# zoxide

## repository

https://github.com/ajeetdsouza/zoxide

## my .bashrc

```bash
eval "$(zoxide init bash)"
```

## version

```
zoxide --version
zoxide 0.9.3
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


## plugins

```
ya pkg add KKV9/compressya pkg add KKV9/compress
```

## version

```
yazi --debug


Yazi
    Version: 26.2.2 (f021aa7a 2026-03-02)
    Debug  : false
    Triple : x86_64-unknown-linux-gnu (linux-x86_64)
    Rustc  : 1.93.1 (01f6ddf7 2026-02-11)

Ya
    Version: No such file or directory (os error 2)

Config
    Init             : /home/kimura/.config/yazi/init.lua (367 chars)
    Yazi             : /home/kimura/.config/yazi/yazi.toml (2195 chars)
    Keymap           : /home/kimura/.config/yazi/keymap.toml (21255 chars)
    Theme            : /home/kimura/.config/yazi/theme.toml (No such file or directory (os error 2))
    VFS              : /home/kimura/.config/yazi/vfs.toml (No such file or directory (os error 2))
    Package          : /home/kimura/.config/yazi/package.toml (No such file or directory (os error 2))
    Dark/light flavor: "" / ""

Emulator
    TERM                : Some("tmux-256color")
    TERM_PROGRAM        : Some("tmux")
    TERM_PROGRAM_VERSION: Some("next-3.7")
    Brand.from_env      : None
    Emulator.detect     : Emulator { kind: Right(Unknown { kgp: false, sixel: false }), version: "", light: false, csi_16t: (0, 0), force_16t: false }

Adapter
    Adapter.matches    : Chafa
    Dimension.available: Dimension { rows: 24, columns: 80, width: 0, height: 0 }

Desktop
    XDG_SESSION_TYPE           : None
    WAYLAND_DISPLAY            : Some("wayland-0")
    DISPLAY                    : Some(":0")
    SWAYSOCK                   : None
    HYPRLAND_INSTANCE_SIGNATURE: None
    WAYFIRE_SOCKET             : None

SSH
    shared.in_ssh_connection: false

WSL
    WSL: true

Variables
    SHELL              : Some("/usr/bin/zsh")
    EDITOR             : None
    VISUAL             : None
    YAZI_FILE_ONE      : None
    YAZI_CONFIG_HOME   : None
    YAZI_ZOXIDE_OPTS   : None
    SSH_AUTH_SOCK      : None
    FZF_DEFAULT_OPTS   : None
    FZF_DEFAULT_COMMAND: None

Text Opener
    default     : Some(OpenerRule { run: "tmux neww \"${EDITOR} \\\"$1\\\"\"", block: true, orphan: false, desc: "Edit", for: None, spread: false })
    block-create: Some(OpenerRule { run: "tmux neww \"${EDITOR} \\\"$1\\\"\"", block: true, orphan: false, desc: "Edit", for: None, spread: false })
    block-rename: Some(OpenerRule { run: "tmux neww \"${EDITOR} \\\"$1\\\"\"", block: true, orphan: false, desc: "Edit", for: None, spread: false })

Multiplexers
    TMUX               : false
    tmux version       : 3.7
    tmux build flags   : enable-sixel=Unsupported
    ZELLIJ_SESSION_NAME: None
    Zellij version     : No such file or directory (os error 2)

Dependencies
    file          : 5.45
    ueberzugpp    : No such file or directory (os error 2)
    ffmpeg/ffprobe: 6.1.1-3 / 6.1.1-3
    pdftoppm      : 24.02.0
    magick        : No such file or directory (os error 2)
    fzf           : 0.70.0
    fd/fdfind     : No such file or directory (os error 2) / 9.0.0
    rg            : 14.1.0
    chafa         : No such file or directory (os error 2)
    zoxide        : 0.9.3
    7zz/7z        : No such file or directory (os error 2) / 23.01
    resvg         : No such file or directory (os error 2)
    jq            : 1.7

Clipboard
    wl-copy/paste: 2.2.1 / 2.2.1
    xclip        : No such file or directory (os error 2)
    xsel         : No such file or directory (os error 2)

Routine
    `file -bL --mime-type`: text/plain


See https://yazi-rs.github.io/docs/plugins/overview#debugging on how to enable logging or debug runtime errors.

```


# neovim

## repository

https://github.com/neovim/neovim

## my AstroNvim

https://github.com/kimurayuuji/astrovim-template

## version
```
nvim --version
NVIM v0.11.6
Build type: Release
LuaJIT 2.1.1741730670
Run "nvim -V1 -v" for more info
```

# lazygit

## repository

https://github.com/jesseduffield/lazygit

## version

```
lazygit --version
commit=1d0db51caf3d280a53f027ef049355fc9e0c57e8, build date=2026-02-07T08:34:27Z, build source=binaryRelease, version=0.59.0, os=linux, arch=amd64, git version=2.43.0
```


# lazydocker

## repository

https://github.com/jesseduffield/lazydocker


# glow

## repository

https://github.com/charmbracelet/glow

# ripgrep

## repository

https://github.com/BurntSushi/ripgrep

## version
```
rg --version
ripgrep 14.1.0

features:-simd-accel,+pcre2
simd(compile):+SSE2,-SSSE3,-AVX2
simd(runtime):+SSE2,+SSSE3,+AVX2

PCRE2 10.42 is available (JIT is available)
```

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

## version

```bash
nb --version
7.25.2
```


# ripgrep-all

## repository

https://github.com/phiresky/ripgrep-all

## installation

https://zenn.dev/dokata/articles/a6d3d1bb308b49

## version

```bash
rga --version
ripgrep-all 0.10.10
```

# zeno.sh

## repositoy

https://github.com/yuki-yano/zeno.zsh


