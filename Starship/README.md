## Starship terminal prompt 

### Prerequisites

- A [Nerd Font](https://www.nerdfonts.com/) installed and enabled in your terminal (for example, try the [Fira Code Nerd Font](https://www.nerdfonts.com/font-downloads)).

### Getting Started

**Note**: due to the proliferation of different platforms, only a subset of supported platforms are
shown below. Can't see yours? Have a look at the [extra platform instructions](https://starship.rs/installing/).

1. Install the **starship** binary:

   #### Install Latest Version

   ##### From prebuilt binary, with Shell:

   ```sh
   sh -c "$(curl -fsSL https://starship.rs/install.sh)"
   ```
   To update the Starship itself, rerun the above script. It will replace the current version without touching Starship's configuration.

   #### Install via Package Manager

   ##### Example: [Homebrew](https://brew.sh/):

   ```sh
   brew install starship
   ```

   ##### With [Scoop](https://scoop.sh):

   ```powershell
   scoop install starship
   ```

2. Add the init script to your shell's config file:

   #### Bash

   Add the following to the end of `~/.bashrc`:

   ```sh
   # ~/.bashrc

   eval "$(starship init bash)"
   ```

   #### Fish

   Add the following to the end of `~/.config/fish/config.fish`:

   ```sh
   # ~/.config/fish/config.fish

   starship init fish | source
   ```

   #### Zsh

   Add the following to the end of `~/.zshrc`:

   ```sh
   # ~/.zshrc

   eval "$(starship init zsh)"
   ```

   #### PowerShell

   Add the following to the end of `Microsoft.PowerShell_profile.ps1`. You can check the location of this file by querying the `$PROFILE` variable in PowerShell. Typically the path is `~\Documents\PowerShell\Microsoft.PowerShell_profile.ps1` or `~/.config/powershell/Microsoft.PowerShell_profile.ps1` on -Nix.

   ```powershell
   Invoke-Expression (&starship init powershell)
   ```

3. After Initializing startship prompt copy run following command and type enter or just reopen terminal
   
    ```sh
    cp -r Startship/.config 
    ```
    

## Official Pages

1) [Official Page](https://starship.rs/)
2) [Github Repository](https://github.com/starship/starship/)