# dot-tmux

my tmux configuration

apt

```sh
sudo apt install tmux
```

yay

```sh
yay -Syu tmux
```

## setup

symlink

```sh
ln -s ~/.config/dot-tmux ~/.config/tmux         # repo

ln -s ~/.config/dot-tmux/tmux.conf ~/.tmux.conf # cfg file
```

don't include plugin files
```sh
echo 'plugins/*' >> .gitignore
```

clone `tpm` from repo:

```sh
$ git clone https://github.com/tmux-plugins/tpm ~/.config/tmux/plugins/tpm
```

init configuration file to use `tpm`:

```sh
set-environment -g TMUX_PLUGIN_MANAGER_PATH '~/.config/tmux/plugins/'   # change plugins install dir

set -g @plugin 'tmux-plugins/tpm'               # plugin manager
set -g @plugin 'tmux-plugins/tmux-sensible'     # plugin

run '~/.config/tmux/plugins/tpm/tpm'            # keep this line at the very bottom of cfg file
```

reload init configuration file

```sh
tmux source ~/.tmux.conf
# OR
:source-file ~/.tmux.conf
```

install plugins

```sh
prefix + I
```

plugins should be installed to `~/.config/tmux/plugins`.

## theme

[theme - tokyo night tmux](https://github.com/janoamaral/tokyo-night-tmux)

## extra

[fzf-theme generator](https://vitormv.github.io/fzf-themes/)
