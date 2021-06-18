## Pre-Process W10 (auto-tuning Windows 10)

The Ansible-Role allows you to perform a series of post-installation manipulations on a freshly installed Windows 10 Pro to configure the basic working environment at home or in the enterprise.

[![License](https://github.com/getsueineko/Ansible-Pre-Process-W10/blob/master/license.svg)](LICENSE)
[![Drone](https://github.com/getsueineko/Ansible-Pre-Process-W10/blob/master/status.svg)](https://github.com/getsueineko/Ansible-Pre-Process-W10/releases)

The role has a modular structure, which makes it easy to customize the desired result, or continue to modify it for yourself.

<p align="center">
  <img src=https://user-images.githubusercontent.com/14312837/121787090-ce4f4300-cbcc-11eb-8701-7a1ccc5c8145.png?raw=true" alt="playbook"/>
</p>

ok - the value of the set variable on the host matches the value in the playbook.
changed - the value of the specified variable on the host did not match the value in the playbook and was changed.
failed - the specified variable cannot be changed.
skipped - checking the value of the specified variable is skipped.                                                                                                              
                                                                                                                                         
## Get started

- [System requirements](https://github.com/getsueineko/Ansible-Pre-Process-W10#System-requirements)
- [Get Pre-Process W10](https://github.com/getsueineko/Ansible-Pre-Process-W10.git)
- [Installation and Usage](https://github.com/getsueineko/Ansible-Pre-Process-W10#installation-and-usage)

## System requirements

Control Server (Windows, Linux, macOS):
1. Python3
2. ```pip install ansible```
3. ```pip install pywinrm[credssp]```

Сontrolled Host (Windows 10):
1. ```ConfigureRemotingForAnsible.ps1 -EnableCredSSP```  
Details [WinRM Setup](https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#winrm-setup)

## Installation and Usage

1. Get all files: ```git clone https://github.com/getsueineko/Ansible-Pre-Process-W10.git```
2. Modify inventory file: ```nano inventory.yml```
3. Modify var file for access to target host: ```nano /group_vars/all.yml```
4. Modify tasks for run: ```nano /Pre-Process W10/roles/common/tasks/Main.yml'```
5. Run ```ansible-playbook pre-process.yml -v```, where number of v is extent of details output: -v - less details, -vv - more details, -vvv - very details

## The brief description of the tasks:

1.  _Install-addtl-pwsh-PackageSources-and-Modules.yml_ - Add Chocolatey and PowerShellGet PackageSources and install some modules like oh-my-posh and Get-ChildItemColor
2.  _Fixes-PowerShell.yml_ - Fix bug with capital letters in the PSReadline module and disable powershell telemetry
3.  _Disable-ReservedStorage.yml_ - Disable Reserved Storage (reserving disk space for future updates)
4.  _Install-Chocolatey.yml_ - Install package manager Chocolatey
5.  _Cinst-BasicSet-Software.yml_ - Install some basic program for work
6.  _Install-Win-BasicFeatures.yml_ - Install basic features like - NetFx3, LegacyComponents, Directplay, TelnetClient, TFTP
7.  _Install-OpenSSH.yml_ - Install OpenSSH (server and client)
8.  _Uninstall-Wordpad-MSPaint.yml_ - Uninstall some legacy components like Wordpad and MSPaint
9.  _Install-MSEdge-(old).yml_ - Install MSEdge (for old win10 releases)
10. _Install-Fonts-(curl).yml_ - Install some useful fonts
11. _Customize-Prompt.yml_ - Customize Prompt (powershell and cmd)
12. _Install-Office-(curl).yml_ - Install Office (default - 2016)
13. _Pull-PostInstall-Folder-(curl).yml_ - Download PostInstall Folder contains some useful utilities
14. _Pin-StartMenu-Apps.yml_ - Pin StartMenu Apps (using xml from PostInstall Folder)
15. _Set-Default-FileAssociations.yml_ - Set Default FileAssociations(using xml from PostInstall Folder)
16. _Setup-Powercfg-Modes.yml_ - Setup Powercfg Modes like High and Max Perfomance (set default high profile)
17. _Clean-SystemDrive.yml_ - Clean temp files
18. _Activate-Win-Office-(encrypted).yml_ - Activate Windows and Office (non including real keys)
19. _Install-Win-Updates-(reboot).yml_ - Install Windows 10 Updates and reboot with notify

TODO List:
- [Show system desktop icons for all users ]
- [Neutral color scheme for all users] 
- [ ] 

## License

Pre-Process W10 is distributed under [GNU GPL 3](LICENSE).
