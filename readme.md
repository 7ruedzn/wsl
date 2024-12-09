# Setup

## Powershell

Download the LTS of powershell with winget:

## Neovim

I use main main neovim setup on WSL + arch, but i also have it installed on windows for quick file editing, if needed

```sh
winget install Neovim.Neovim
```

After getting neovim, i like to use the neovim distro nvchad:

```sh
git clone https://github.com/NvChad/starter $ENV:USERPROFILE\AppData\Local\nvim && nvim
```

## Starship
Download starship in windows using by running the command on powershell:

```sh
winget install --id Starship.Starship
```

Install Terminal Icons on powershell

```sh
Install-Module -Name Terminal-Icons -Repository PSGallery
```

Open your profile to set the configurations

```sh
notepad $PROFILE #open profile with editor (code, notepad, etc)
```

Add these into your $PROFILE

```sh
Import-Module -Name Terminal-Icons
Remove-Item Alias:ls -ErrorAction SilentlyContinue
Function ls { Get-ChildItem | Format-Wide }
Invoke-Expression (&starship init powershell)
```

## Nerd font
Download the JetbrainsMono Nerd font on this link [JetbrainsMono Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/JetBrainsMono.zip) and install it.

## Windows terminal
Download windows terminal from the microsoft store. Open it and paste the JSON into your windows terminal settings. You can find the settings JSON by right clicking on the down arrow on the top bar -> settings -> open JSON file.

This JSON will set the configurations and themes to your windows terminal.

```json
{
    "$help": "https://aka.ms/terminal-documentation",
    "$schema": "https://aka.ms/terminal-profiles-schema",
    "actions": 
    [
        {
            "command": 
            {
                "action": "copy",
                "singleLine": false
            },
            "id": "User.copy.644BA8F2",
            "keys": "ctrl+c"
        },
        {
            "command": "paste",
            "id": "User.paste",
            "keys": "ctrl+v"
        },
        {
            "command": "find",
            "id": "User.find",
            "keys": "ctrl+shift+f"
        },
        {
            "command": 
            {
                "action": "splitPane",
                "split": "auto",
                "splitMode": "duplicate"
            },
            "id": "User.splitPane.A6751878",
            "keys": "alt+shift+d"
        }
    ],
    "alwaysShowNotificationIcon": true,
    "alwaysShowTabs": true,
    "centerOnLaunch": true,
    "copyFormatting": "none",
    "copyOnSelect": true,
    "defaultProfile": "{a5a97cb8-8961-5535-816d-772efe0c6a3f}",
    "focusFollowMouse": true,
    "initialCols": 160,
    "initialPosition": ",",
    "initialRows": 40,
    "launchMode": "default",
    "newTabMenu": 
    [
        {
            "type": "remainingProfiles"
        }
    ],
    "profiles": 
    {
        "defaults": 
        {
            "colorScheme": "Tokyo Night Storm",
            "elevate": true,
            "font": 
            {
                "builtinGlyphs": false,
                "face": "JetBrains Mono NL"
            },
            "tabTitle": null
        },
        "list": 
        [
            {
                "commandline": "%SystemRoot%\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
                "font": 
                {
                    "face": "JetBrainsMono Nerd Font"
                },
                "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
                "hidden": false,
                "name": "Windows PowerShell"
            },
            {
                "commandline": "%SystemRoot%\\System32\\cmd.exe",
                "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
                "hidden": false,
                "name": "Command Prompt"
            },
            {
                "guid": "{b453ae62-4e3d-5e58-b989-0a998ec441b8}",
                "hidden": true,
                "name": "Azure Cloud Shell",
                "source": "Windows.Terminal.Azure"
            },
            {
                "guid": "{2ece5bfe-50ed-5f3a-ab87-5cd4baafed2b}",
                "hidden": false,
                "name": "Git Bash",
                "source": "Git"
            },
            {
                "guid": "{51855cb2-8cce-5362-8f54-464b92b32386}",
                "hidden": true,
                "name": "Ubuntu",
                "source": "CanonicalGroupLimited.Ubuntu_79rhkp1fndgsc"
            },
            {
                "guid": "{2c4de342-38b7-51cf-b940-2309a097f518}",
                "hidden": true,
                "name": "Ubuntu",
                "source": "Windows.Terminal.Wsl"
            },
            {
                "colorScheme": "Tokyo Night Storm",
                "cursorShape": "filledBox",
                "elevate": true,
                "experimental.retroTerminalEffect": false,
                "font": 
                {
                    "builtinGlyphs": false,
                    "face": "JetBrainsMono Nerd Font"
                },
                "guid": "{a5a97cb8-8961-5535-816d-772efe0c6a3f}",
                "hidden": false,
                "icon": "C:\\Users\\vinicius.q.filipe\\Documents\\arch logo.png",
                "name": "arch",
                "padding": "0",
                "scrollbarState": "hidden",
                "source": "Windows.Terminal.Wsl",
                "suppressApplicationTitle": true,
                "tabTitle": "arch",
                "useAcrylic": true
            },
            {
                "guid": "{28d1d9df-296c-5d52-ac5f-e99b6879ae56}",
                "hidden": true,
                "name": "Developer Command Prompt for VS 2022",
                "source": "Windows.Terminal.VisualStudio"
            },
            {
                "guid": "{a8d6f533-efda-5c2b-aade-c1dce5df79ff}",
                "hidden": true,
                "name": "Developer PowerShell for VS 2022",
                "source": "Windows.Terminal.VisualStudio"
            },
            {
                "guid": "{16208362-94fc-5b1f-a491-5b2624d5ab56}",
                "hidden": true,
                "name": "Visual Studio Debug Console",
                "source": "VSDebugConsole"
            }
        ]
    },
    "schemes": 
    [
        {
            "background": "#24283B",
            "black": "#414868",
            "blue": "#7AA2F7",
            "brightBlack": "#414868",
            "brightBlue": "#7AA2F7",
            "brightCyan": "#7DCFFF",
            "brightGreen": "#73DACA",
            "brightPurple": "#BB9AF7",
            "brightRed": "#F7768E",
            "brightWhite": "#C0CAF5",
            "brightYellow": "#E0AF68",
            "cursorColor": "#C0CAF5",
            "cyan": "#7DCFFF",
            "foreground": "#A9B1DC",
            "green": "#73DACA",
            "name": "Tokyo Night Storm",
            "purple": "#BB9AF7",
            "red": "#F7768E",
            "selectionBackground": "#28344A",
            "white": "#C0CAF5",
            "yellow": "#E0AF68"
        }
    ],
    "showTabsInTitlebar": true,
    "startOnUserLogin": true,
    "themes": [],
    "useAcrylicInTabRow": true
}
```

## Arch WSL
Arch wsl is yet not available in the official WSL distros by microsoft. To check the available distros, run the following on powershell:

```sh
wsl --list --online
```

next you will need to install the wsl on your system by the following command. It will install the default distro, that is currently Ubuntu, but we will install the arch next. Later you can remove the Ubuntu profile on your windows terminal.

```sh
wsl --install
```

When it finishes installing, please reboot your machine. If you don't reboot, the arch WSL won't be able to be installed.

After rebooting, this repo has implemented the arch distro on WSL [ArchWSL](https://github.com/yuk7/ArchWSL). To install it correctly, please follow the docs on the readme provided by the author: [Arch WSL install guide](https://wsldl-pg.github.io/ArchW-docs/How-to-Setup/)

After installing arch on WSL, you can rice it by using my dotfiles with GNU stow: [dotfiles](https://github.com/7ruedzn/dotfiles)

## QOL settings on WSL

windows appends paths while typing for commands, so it can cause a lot of input lag, and also resets the hosts and resolv.conf on every instance of WSL. Add the following to the ```/etc/wsl.conf``` on WSL to fix those issues:
   
```sh
[interop]
appendWindowsPath = false

[network]
generateResolvConf = false
generateHosts = false
```
