# ZSH custom configuration

## Installing zsh as default shell

If necessary, follow these steps to install Zsh:

1. There are two main ways to install Zsh
  - with the package manager of your choice, _e.g._ `sudo apt install zsh` (see [below for more examples](#how-to-install-zsh-on-many-platforms))
  - from [source](http://zsh.sourceforge.net/Arc/source.html), following
        [instructions from the Zsh FAQ](http://zsh.sourceforge.net/FAQ/zshfaq01.html#l7)
2. Verify installation by running `zsh --version`. Expected result: `zsh 5.4.2` or more recent.
3. Make it your default shell: `chsh -s $(which zsh)`
  - Note that this will not work if Zsh is not in your authorized shells list (`/etc/shells`)
    or if you don't have permission to use `chsh`. If that's the case [you'll need to use a different procedure](https://www.google.com/search?q=zsh+default+without+chsh).
4. Log out and log back in again to use your new default shell.
5. Test that it worked with `echo $SHELL`. Expected result: `/bin/zsh` or similar.
6. Test with `$SHELL --version`. Expected result: 'zsh 5.4.2' or similar

> **Ubuntu, Debian** & derivatives (Windows 10 WSL | Native Linux kernel with Windows 10 **build 1903**)

```sh
apt install zsh
```

If you don't have `apt`, the recommended package manager for end users
[ [1] ](http://askubuntu.com/a/446484)
[ [2] ](http://askubuntu.com/a/775264)
[ [3] ](https://help.ubuntu.com/lts/serverguide/apt.html)
[ [4] ](http://www.howtogeek.com/234583/simplify-command-line-package-management-with-apt-instead-of-apt-get/)
, you can try `apt-get` or `aptitude`.

## Installing Oh My Zsh

Once you have zsh, you can install Oh My Zsh, by simply running one of these commands:

  | Method    | Command                                                                                           |
  |:----------|:--------------------------------------------------------------------------------------------------|
  | **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
  | **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
  | **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

## Installing custom themes

You can use built-in in themes or can use custom themes, which are stored in [themes](./themes) folder.

To use them run 
```bash
cp ./ZSH/themes/* ~/.oh-my-zsh/themes
```
 After that modify `~/.zshrc` variable `ZSH_THEME=` to `ZSH_THEME="theme-name"`

## Installing plugins

Plugins can be installed by copying folder containing file with `.plugin.zsh` extension to the `~/.oh-my-zsh/plugins`.

After that just add plugin name to the `.zshrc` file at section `plugins=(plugin-name ...)`

## Installing custom *`.zshrc`*

To use custom Oh-My-Zsh configuration instead of default run following commands

```sh
mv ~/.zshrc ~/.zshrc.backup
cp ./ZSH/.zshrc ~/.zshrc
source ~/.zshrc
```

If you want to use default default configuration and setup it manualy just run following commands

```sh
mv ~/.zshrc ~/.zshrc.backup.old
mv ~/.zshrc.backup ~/.zshrc
source ~/.zshrc
```

# Links

- [Oh My ZSH official page](https://ohmyz.sh/)
- [Oh My ZSH github](https://github.com/ohmyzsh/ohmyzsh/)