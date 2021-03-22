# Tmux custom config

## Installing tmux

Check [official tmux wiki](https://github.com/tmux/tmux/wiki) to install it correctly and last version.

## Installing plugins

To install tmux plugins for perform this steps

Copy content from `Tmux/.tmux/`
```bash
cp -r ./Tmux/.tmux/ ~/.tmux/
```

Replace existing `~/.tmux.conf` with configuration stored at `Tmux/`

```bash
cp ./Tmux/.tmux.conf .tmux.conf.local ~/
```

Reload TMUX environment so TPM is sourced:

```bash
# type this in terminal if tmux is already running
$ tmux source ~/.tmux.conf
```

That's it!

### Installing plugins

1. Add new plugin to `~/.tmux.conf` with `set -g @plugin '...'`
2. Press `prefix` + <kbd>I</kbd> (capital i, as in **I**nstall) to fetch the plugin.

You're good to go! The plugin was cloned to `~/.tmux/plugins/` dir and sourced.
