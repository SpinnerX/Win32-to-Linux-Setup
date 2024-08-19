# Win32-to-Linux-Setup
Configurations for a Linux-like experience on Windows

 ## Installation

 ## Powershell no titlebar

 - To get rid of the powershell titlebar simply go to settings and appearence and them toggle off title bar to hide it.

 - Here are the keybindings to open up a new terminal session.
 - Ctrl+Shift 1 -> Windows Powershell
 - Ctrl+Shift 2 -> Command Prompt
 - Ctrl+Shift 6 -> Powershell (in Profile 1 session)
 - Ctrl+Shift 7 -> Powershell (in Profile 1 admin mode session)
 - Ctrl+, -> to go into settings (literally type `ctrl` key and the `,` comma key)

 ## For installing oh-my-posh

 - The themes directory is `C:\Program Files (x86)\oh-my-posh\themes`

 - How you reference to your themes in the windows powershell profile is by referencing to `$env:POSH_THEMES_PATH`

 - In that configuration file to configure oh-my-posh
   
 - This is how you configure a specific theme: `oh-my-posh init pwsh --config $env:POSH_THEMES_PATH/capr4n.omp.json | Invoke-Expression`

## New themes that DO NOT COME WITH OH-MY-POSH DEFAULT THEMES

- Link where I found the nord themes, `https://github.com/AntonRyadovoy/pwsh_profile`

- Nord themes
   * These are nord-related themes available
     
   * `nordcustom_v`
     
   * `nordcustom`
     
   * `nordcustom_v.3`

## Configurating Desktop Layout, Widgets, Applets
- For configurations purpose make sure to have your directory called `My-Desktop-Configurations` in the C drive.

- So the filepath to that directory should look like `C:\My-Desktop-Configurations\neofetch-logos` or whatever directory you want to access here.

First install TaskbarXI

- Go to the binaries and install `TaskbarXI.exe` and `TaskbarXGUI.exe`

- Then create directory inside local C drive (C:) called `My-Desktop-Configurations`

- Once directory is created then copy and paste those two binaries into this new directory.

Second installing Rainmeter and Droptop four

- To install rainmeter go to this website https://www.rainmeter.net/

- To install droptop four go to this website here https://droptopfour.com/

Install JaXCor

- Then install `ModularVisualizer` and `ModularClocks`

- Once installed go ahead and choose the theme and toggle to enable them.

## Installing Winfetch

- This is window's equivalent to neofetch just for windows...

- To find the config file will be located at this default file location `$env:USERPROFILE/.config/winfetch/config.ps1`

- Just do `cd $env:USERPROFILE/.config/winfetch/config.ps1` and it'll take you to the file

- Then change the `$image` variable to the location of the image file that contains the image file.

## Removing titlebar in Windows 11

- Install ing autohotkey 1.1
- Link is `https://www.autohotkey.com/`

- Then once you install the link double-click the script `script/no-titlebar.ahk`

- Which should have a small window popup and disappear and thats it!

## Links
Link to devianart for website art - https://www.deviantart.com

Link to wallpapercave for more art for wallpapers - https://wallpapercave.com

## Windows Key Shortcuts (Keybindings)

`Alt+Tab` is for changing different window page tabs.

`Alt+F4` is for closing current(single) page.


## If $PROFILE is empty copy this below

- Setting terminal configurations to these default configuration lines. (that get ran at the start of each terminal session)

- Wer are setting the `oh-my-posh` theme to tokyo night storm theme.

- We are setting winfetch to the alias name of `neofetch` to match unix-compliant naming conventions for my sanity (LOL)

```powershell

# Just an example
# $env:POSH_THEMES_PATH/jandedobbeleer.omp.json

# Do this one
oh-my-posh init pwsh --config $env:POSH_THEMES_PATH/capr4n.omp.json | Invoke-Expression

Set-Alias -Name neofetch -Value winfetch

```
