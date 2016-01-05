#Windows

This repository contains information and instructions on my standard Windows configuration. This is a comprehensive guide to setting up everything I could possibly need in a given Windows environment.

Direct download links are provided where possible.

##Applications

These applications need to be installed manually.

- [Chocolatey](https://chocolatey.org/) for nearly painless package management
- [Notation](http://getnotation.com/) for synchronising notes with Simplenote

### Home
- [SunVox](http://www.warmplace.ru/soft/sunvox/) for making wacky modtracker-esque music
- [Grafx2](https://code.google.com/p/grafx2/downloads/list?can=2&q=label%3AOpSys-Windows+label%3ARelease-2.4) for drawing layered pixel art

### Work
- [SenchaCmd 4.0.5](https://cdn.sencha.com/cmd/4.0.5.87/SenchaCmd-4.0.5.87-windows.exe.zip) for building ExtJS web apps at work. **Requires work Chocolately script to have been run as that installs Ruby**
- [SmartSVN](http://www.smartsvn.com/)

###Games

For fun and stuff.

- [Factorio](https://www.factorio.com/login) (log in to download)
- [Minecraft](https://launcher.mojang.com/download/MinecraftInstaller.msi) (.msi link)

##Ninite
Although use of Ninite is mostly deprecated by Chocolatey, it's still better at installing a handful of applications as Chocolatey support is a bit patchy for things like iTunes and Spotify. Until these issues are resolved, I'll be using Ninite for the following software.

- iTunes - I'll need to import my iTunes library
- Spotify

##Packages
I now use [Chocolatey](https://chocolatey.org/) to install most of my software on Windows. There are three scripts in this repository for installing environment pertinent software packages.

### install-general.bat
- less
- googlechrome - default browser
- maven - java dependency management
- jdk - x64 JDK (includes JRE)
- sublimetext3 
- sublimetext3.packagecontrol 
- ubuntu.font - Ubuntu font family package for use in Sublime Text
- flashplayerplugin - to make it slightly easier to browse shitty parts of the internet
- 7zip
- sourcetree - great git client
- firefox - backup browser
- filezilla 
- silverlight 
- wget 
- intellijidea-community - i am so happy that there is a package for this
- vim 
- putty 
- libreoffice 
- dotnet4.5 
- adobereader
- adobeshockwaveplayer - another dated web technology
- dropbox 
- virtualbox 
- svn 
- adobeair 
- thunderbird - for doing emails
- magicdisc - for mounting iso files
- python 
- 1password 
- gyazo 
- f.lux 
- deluge - torrents

### install-home.bat
- steam
- cccp
- mpc-hc
- paint.net
- blender
- teamspeak
- mumble
- unity
- youtube-dl

### install-work.bat
- tomcat 
- mysql.workbench
- kdiff3 
- slack 
- ruby - for Sencha CMD)
- jdk (x86) - because Eclipse/STS is a shit

##Configuration steps (needs work)

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
- Run Chocolatey scripts

##Ninite

**DEPRECATED. CURRENTLY A FAILSAFE FOR CHOCOLATEY PACKAGES THAT FAIL TO INSTALL**

[Ninite](http://www.ninite.com) allows silent installation of many common software packages. I've omitted links for now. Select the following packages:

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

## Retired packages
- [GitHub for Windows](https://desktop.github.com/) - it keeps failing me, is severely limited, and SourceTree is better and does way more