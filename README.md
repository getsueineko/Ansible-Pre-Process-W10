## Pre-Process W10 (auto-tuning Windows 10)

The Ansible-Role allows you to perform a series of post-installation manipulations on a freshly installed Windows 10 Pro to configure the basic working environment at home or in the enterprise.

[![License](https://github.com/getsueineko/Ansible-Pre-Process-W10/blob/master/license.svg)](LICENSE)
[![Drone](https://github.com/getsueineko/Ansible-Pre-Process-W10/blob/master/status.svg)](link)

The role has a modular structure, which makes it easy to customize the desired result, or continue to modify it for yourself.

## Get started

- [Get Pre-Process W10](link)
- [Installation and Usage Guides](link)

## Installation and Usage
1. ```git clone https://github.com/getsueineko/Ansible-Pre-Process-W10.git```
2. Modify inventory file ```nano inventory.yml```
3. Modify tasks for run via ```nano '.\Pre-Process W10\roles\common\tasks\Main.yml'```
4. Run ansible-playbook pre-process.yml -vvv

---

A brief description of the manipulations:
1.  Install-addtl-pwsh-PackageSources-and-Modules.yml - Add Chocolatey and PowerShellGet PackageSources and install some modules like oh-my-posh and Get-ChildItemColor
2.  Fixes-PowerShell.yml - Fix bug with capital letters in the PSReadline module and disable powershell telemetry
3.  Disable-ReservedStorage.yml - Disable Reserved Storage (reserving disk space for future updates)
4.  Install-Chocolatey.yml - Install package manager Chocolatey
5.  Cinst-BasicSet-Software.yml - Install some basic program for work
6.  Install-Win-BasicFeatures.yml - Install basic features like - NetFx3, LegacyComponents, Directplay, TelnetClient, TFTP
7.  Install-OpenSSH.yml - Install OpenSSH (server and client)
8.  Uninstall-Wordpad-MSPaint.yml - Uninstall some legacy components like Wordpad and MSPaint
9.  Install-MSEdge.yml - Install MSEdge (for old win10 releases)
10. Install-Fonts-(curl).yml - Install some useful fonts
11. Customize-Prompt.yml - Customize Prompt (powershell and cmd)
12. Install-Office-(curl).yml - Install Office (default - 2016)
13. Pull-PostInstall-Folder-(curl).yml - Download PostInstall Folder contains some useful utilities
14. Pin-StartMenu-Apps.yml - Pin StartMenu Apps (using xml from PostInstall Folder)
15. Set-Default-FileAssociations.yml - Set Default FileAssociations(using xml from PostInstall Folder)
16. Setup-Powercfg-Modes.yml - Setup Powercfg Modes like High and Max Perfomance (set default high profile)
17. Clean-SystemDrive.yml - Clean temp files
18. Activate-Win-Office-(encrypted).yml - Activate Win Office (non including real keys)
19. Install-Win-Updates-(reboot).yml - Install Windows 10 Updates and reboot with notify

TODO List:
- [Show system desktop icons for all users ]
- [Neutral color scheme for all users] 
- [ ] 

## License

Pre-Process W10 is distributed under [AGPL-3.0-only](LICENSE).
