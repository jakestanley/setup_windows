# Windows

This repository contains information and instructions on my standard Windows configuration. This is a comprehensive guide to setting up everything I could possibly need in a given Windows environment. Configuration is for Windows 10 - 10th April, 2016.

Direct download links are provided where possible.

## tl;dr setup

- Configure partitions
- Install [Chocolatey](https://chocolatey.org/)
- Run the install scripts starting with `install-general.bat`
- Install manual installation software
- Perform "Addition Configuration Steps"

## Manual installation required

These applications need to be installed manually as they are not available or are unstable in the chocolatey repositories.

### General

- [Chocolatey](https://chocolatey.org/) for nearly painless package management. i advise you install this first, then run the scripts, then install the other manual stuff.
- [Notation](http://getnotation.com/) for synchronising notes with Simplenote
- [Magicdisc](http://www.magiciso.com/tutorials/miso-magicdisc-overview.htm) as the Chocolatey package currently doesn't work. It doesn't install the driver or something
- [iTunes](http://itunes.com/) for use at home because that's where I sync my iThings *rms term used ironically*
- [Spotify](https://www.spotify.com/download/)
- [Toggl](https://support.toggl.com/toggl-desktop-for-windows/) - for keeping track of my time spent on projects

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
- jdk - will install the x86 or x64 version depending on your platform
- sublimetext3
- sublimetext3.packagecontrol
- atom - open source text editor from Github
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
- python - *temporarily removed. should be replaced with python2 when that decides to work*
- 1password
- gyazo
- f.lux
- deluge - torrents
- cygwin
- btsync - BitTorrent Sync
- winmerge
- pandoc
- nodejs
- explorerplusplus
- cyg-get - package manager for cygwin
- poshgit - fancy git command line thingy
- winrar - because it's good for those split rar files
- conemu - all your terminal emulators in one place
- clink - makes using terminal emulators nicer
- lightshot - my new favourite screenshot program. // TODO phase out gyazo
- autohotkey - for macros and disabling caps lock // TODO look into automating more stuff
- ccleaner - keeps things clean

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
- obs - open broadcaster software

### install-work.bat // TODO update
- tomcat
- mysql
- mysql.utilities
- mysql.workbench
- slack
- svn
- ruby - for Sencha CMD)
- eclipse - Chocolatey should install the appropriate architecture version
- googledrive - I can just use my work Google account to keep files in sync
- thunderbird - for doing emails (at work)
- tortoisesvn
- jdk (x86) - just in case the 32-bit JDK is needed for Eclipse or Spring, etc

## Additional configuration steps

- clone [dotfiles](https://github.com/madstanners/dotfiles) repository and run `dotfiles.bat`
- [disable OneDrive](https://techjourney.net/disable-or-uninstall-onedrive-completely-in-windows-10/)
- [remove homegroup](http://www.howtogeek.com/howto/27091/how-to-disable-or-enable-the-homegroup-feature-in-windows-7/) - guide is for Windows 7 but also works on 10
- [remove Windows 10 apps](http://www.howtogeek.com/224798/how-to-uninstall-windows-10s-built-in-apps-and-how-to-reinstall-them/)
- [alias dir to ls in cmd](http://stackoverflow.com/a/15043472)
- [disable automatic updates](http://lifehacker.com/prevent-windows-10-from-automatically-restarting-your-p-1723647582)
- set browser [homepage](https://github.com/madstanners/homepage)
- remove bullshit tiles from the start menu
- set Explorer++ as the default file manager
- You might need to reinstall the sublime package control chocolatey package at this point
- Partition drives (see below)
- Set up FileHistory on separate drive and restore data if necessary
- Configure BitTorrent Sync - see note on simplenote.com
- Relocate default "Documents", "Downloads", and "Music" folders to the separate drive
- Configure paging file
- Set power options and disable random waking from sleep
- Configure VPN profile for work (if applicable)
- Install manual software
- Set Steam libraries

###Partitioning drives

I've had numerous problems with Windows in the past and I now try to keep the OS partition containing as little user created data as possible, to reduce the amount of faff when I inevitably reinstall. The following partition scheme is what I aim to use.
- 100GB (minimum) operating system and applications drive. consider using this for games too, as they can be redownloaded
- Separate partition - ideally on a different physical drive - for documents and other data