#Windows

This repository contains information and instructions on my standard Windows configuration. This is a comprehensive guide to setting up everything I could possibly need in a Windows environment.

Direct download links are provided where possible.

##Applications

Comprehensive list of stuff I need to install.

- [Notation](http://getnotation.com/)
- [Grafx2](https://code.google.com/p/grafx2/downloads/list?can=2&q=label%3AOpSys-Windows+label%3ARelease-2.4) - for drawing layered pixel art
- [Blender](https://www.blender.org/download/) - for 3D modelling
- [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)
- [Sublime Text 3](http://www.sublimetext.com/3)
- [Gyazo](https://gyazo.com/download?dl=now) - for quick sharing screenshots
- [f.lux](https://justgetflux.com/dlwin.html) - easy on the eyes
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) - for VMs
- [deluge](http://download.deluge-torrent.org/windows/?C=M;O=D) - bittorrent client
- [Mumble](http://wiki.mumble.info/wiki/Main_Page#Download_Mumble) - a VoIP client
- [SunVox](http://www.warmplace.ru/soft/sunvox/)
- [Ubuntu Mono font](http://font.ubuntu.com/) - for programming
- [SourceTree](https://www.sourcetreeapp.com/download/) - Git client by Atlassian

###Soon to be retired
- [TeamSpeak 3](https://www.teamspeak.com/downloads) - soon to be retired in favour of Mumble, which is secure and open source
- [GitHub for Windows](https://desktop.github.com/) - it keeps failing me, and SourceTree is better

##Packages
I use [Chocolatey](https://chocolatey.org/) to install packages on Windows. Install that, then install the following with ```cinst```
- wget
- git
- less
- vim

##Games

For fun and stuff.

- [Factorio](https://www.factorio.com/login) (log in to download)
- [Minecraft](https://launcher.mojang.com/download/MinecraftInstaller.msi) (.msi link)

##Ninite

[Ninite](http://www.ninite.com) allows silent installation of many common software packages. I've omitted links for now. Select the following packages:

- Chrome - main browser
- CCCP (Includes MPC. Trying this instead of VLC)
- PuTTY
- 7-Zip - WinRAR without the guilt
- Steam
- iTunes (I need to import my iTunes library)
- Spotify
- Paint.NET - best drawing tool on Windows IMO
- LibreOffice
- Adobe Reader
- Dropbox
- TeamViewer
- Firefox - backup browser
- FileZilla
- WinMerge - trying this one too as a Windows alternative to Kdiff3

###Runtimes via Ninite

Ninite can install the following runtimes so I select these too. There's less chance of chaffing when doing stuff in Windows if you install these ballache dependencies in advance.

- .NET
- Java x64 JDK (Includes JRE)
- Silverlight
- Adobe Air
- Shockwave

##Configuration steps

- My 'dotfiles' repository now has a batch script for linking files. Run this from the dotfiles directory
- Disable Internet Explorer and/or Microsoft Edge
- Partition drives and create Linux boot partition (if applicable)
- Configure paging file
- Set power options and disable random waking from sleep
- Configure VPN profile for work (if applicable)
- Set wallpaper
- Install software
- Set Steam library
- Set Steam games off downloading
