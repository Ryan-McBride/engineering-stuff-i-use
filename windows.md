always use the latest version of windows with updates. There's this weird meme in the windows community that whatever that lates build is ruined everything, but the best way to keep your environment clean and free from vulnerabilities is to keep everything updated.

ninite: is what I use for getting a new install up to date

powertoys: tiling window manager and batch rename tools

terminus: terminal emulator

chocolatey: package manager
  git
  vim
  python

generate ssh:
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
ssh-agent -s
ssh-add .ssh/id_rsa
clip < .ssh/id_rsa.pub


vundle is installed differently on windows: https://github.com/VundleVim/Vundle.vim/wiki/Vundle-for-Windows

additionally, utilisnips plugin must be removed from the vrc, and `set t_Co=256` needs to be added to the vrc for colors to work correctly

posh-git:

Install-Module posh-git
Add-PoshGitToProfile
