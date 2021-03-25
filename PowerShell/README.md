# PowerShell Settings

## Installation
Contains this steps:

1) [Fonts](#fonts-install)
2) [Custom Themes](#custom-themes-install)
3) [User Profile](#user-profile-install)

## Fonts install

To install fonts, which will correctly display unusual symbols just open this fonts folder via explorer at `C:\Windows\Fonts`, then just drag and drop all content from [Fonsts](./Fonts/Meslo) folder

## Custom themes install

[Themes](./Themes) contains modified themes which can be used insted of predifened themes. To use them

- Create folder at user root directory
- Copy themes to this folder

After that you can use them by executing this command

```ps1
Set-PoshPrompt -Theme "<theme-path-here>"
```

Theme path can be relative `~\Path-to-theme` or absolute `C:\Users\username\Path-to-theme`

## User profile install

To setup userprofile, which is loaded at start of each new PowerShell session:

- Open PowerShell `Win + r`
- Enter `powershell`
- Execute 
    ```ps1
    notepad $profile
    ```

 After opening userprofile with notepad copy [file content](./UserProfile/Microsoft.PowerShell_profile.ps1) to opened file or just enter this lines of code

 ```ps1
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme ~\CustomPoshThemes\honukai_custom.omp.json
 ```

 If you want to use one of the built-in themes just type in PowerShell session `Get-PoshThemes`. This command will display build-in themes appearance and names, after this just copy theme name and replace last paramenter at 

 ```ps1
Set-PoshPrompt -Theme "<theme-name-here>"
 ```

