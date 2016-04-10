# Windows

This repository contains information and instructions on my standard Windows configuration. This is a comprehensive guide to setting up everything I could possibly need in a given Windows environment.

Direct download links are provided where possible.

## Manual installation required

These applications need to be installed manually as they are not available or are unstable in the chocolatey repositories.

### General

- [Chocolatey](https://chocolatey.org/) for nearly painless package management
- [Notation](http://getnotation.com/) for synchronising notes with Simplenote
- [Magicdisc](http://www.magiciso.com/tutorials/miso-magicdisc-overview.htm) as the Chocolatey package currently doesn't work. It doesn't install the driver or something
- [iTunes](http://itunes.com/) for use at home because that's where I sync my iThings *rms term used ironically*
- [Spotify](https://www.spotify.com/download/)

#### Python/Python2/PIP
"pip is already installed if you're using Python 2 >=2.7.9 or Python 3 >=3.4 downloaded from [python.org](http://python.org/), but you'll need to upgrade pip" - https://pip.pypa.io/en/stable/installing/

### Home
- [SunVox](http://www.warmplace.ru/soft/sunvox/) for making wacky modtracker-esque music
- [tagspaces](http://www.tagspaces.org/downloads/) for keeping tabs on folder structures - trialling this for now

### Work
- [SenchaCmd 4.0.5](https://cdn.sencha.com/cmd/4.0.5.87/SenchaCmd-4.0.5.87-windows.exe.zip) for building ExtJS web apps at work. **Requires work Chocolately script to have been run as that installs Ruby**

### Games
- [Factorio](https://www.factorio.com/login) (log in to download) - now on Steam
- [Minecraft](https://launcher.mojang.com/download/MinecraftInstaller.msi) (.msi link)
- [Origin](https://www.origin.com/en-gb/download) Steam for EA Games

## Packages
I now use [Chocolatey](https://chocolatey.org/) to install most of my software on Windows. There are three scripts in this repository for installing environment pertinent software packages.

### install-general.bat // TODO update
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
- git - obviously
- putty
- libreoffice
- dotnet4.5
- adobereader
- adobeshockwaveplayer - another dated web technology
- dropbox
- virtualbox
- adobeair
- thunderbird - for doing emails
- python - *temporarily removed. should be replaced with python2 when that decides to work*
- 1password
- gyazo
- f.lux
- deluge - torrents
- cygwin
- btsync - BitTorrent Sync
- winmerge
- pandoc

### install-home.bat
- steam
- cccp
- mpc-hc
- paint.net
- blender
- handbrake - for video encoding
- teamspeak
- mumble
- unity
- youtube-dl
- goggalaxy - Steam-like client for Good Old Games

### install-work.bat // TODO update
- tomcat
- mysql
- mysql.utilities
- mysql.workbench
- kdiff3
- slack
- svn
- ruby - for Sencha CMD)
- eclipse - Chocolatey should install the appropriate architecture version
- jdk (x86) - just in case the 32-bit JDK is needed for Eclipse or Spring, etc

##Configuration steps (needs work)

- Run Chocolatey scripts
- My 'dotfiles' repository now has a batch script for linking files. Run this from the dotfiles directory
- You might need to reinstall the sublime package control chocolatey package at this point
- Partition drives (see below)
- Set up FileHistory on separate drive and restore data if necessary
- Configure BitTorrent Sync - see note on simplenote.com
- Relocate default "Documents", "Downloads", and "Music" folders to the separate drive
- Configure paging file
- Set power options and disable random waking from sleep
- Configure VPN profile for work (if applicable)
- Set wallpaper
- Install manual software
- Set Steam libraries

###Partitioning drives

I've had numerous problems with Windows in the past and I now try to keep the OS partition containing as little user created data as possible, to reduce the amount of faff when I inevitably reinstall. The following partition scheme is what I aim to use.
- 100GB (minimum) operating system and applications drive. consider using this for games too, as they can be redownloaded
- Separate partition - ideally on a different physical drive - for documents and other data

#Deprecated

**DEPRECATED. FOR FAILSAFE USE ONLY**

##Ninite

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