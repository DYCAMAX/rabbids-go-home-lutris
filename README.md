![Game Cover](/Cover.jpg)
# Play Rabbids Go Home on Linux
C'est un guide qui permet d'installer la version windows de [Rabbids Go Home]( plus facilement sur linux 
# Reqirements
- [Lutris](https://lutris.net/downloads/)
- [CDEmu](https://cdemu.sourceforge.io/)
- Rabbids Go Home as disc or iso
- Vulkan capable GPU, and Driver for DXVK Support
# Installation

## Install Lutris and Wine dependencies
These steps will heavily depend on your Linux distribution. Lutris has great documentation covering these which I've linked against each.
1. [Lutris](https://lutris.net/downloads/)
2. [Wine Dependencies](https://github.com/lutris/docs/blob/master/WineDependencies.md)
3. [Drivers](https://github.com/lutris/docs/blob/master/InstallingDrivers.md) (needed for DXVK Support)

## Install 32-bit GStreamer
Without these dependencies the in game videos won't play, and throw an error.
- Ubuntu or Debian:
```
apt-get install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio
```
- Fedora:
```
dnf install gstreamer1-devel gstreamer1-plugins-base-tools gstreamer1-doc gstreamer1-plugins-base-devel gstreamer1-plugins-good gstreamer1-plugins-good-extras gstreamer1-plugins-ugly gstreamer1-plugins-bad-free gstreamer1-plugins-bad-free-devel gstreamer1-plugins-bad-free-extras
```
## Using CDEmu (If using ISO)
[CDemu](https://cdemu.sourceforge.io/) is a software suite designed to emulate an optical drive and disc (including CD-ROMs and DVD-ROMs) on the Linux operating system.
- Install CDemu, refer online for steps that cover your distribution
- Once installed check CDemu status with `cdemu status`
- Load the install image in one devices
```
cdemu load 0 /Your Folder/YourRabbidsGoHomeFiles.iso
```
## Running the Lutris installer
There is a few different ways you can start the installer these are listed below. You only need to do one of them.

- From the Lutris website
1. Select the Install button on the Rabbids Go Home page for the DVD version
- From the Lutris app
1. Select the Lutris source on the right
2. Search for "Rabbids Go Home" under the Community Installers tab
3. Select Install for "Rabbids Go Home"
- Local with the install script
1. Download the Lutris install script rabbids-go-home.yml
2. Select "Add Games" on Lutris
3. Select the option "Download from a local installation script"
4. Select your rabbids-go-home.yml file.

If you installed the game with CDemu, make sure to unload the discs afterwards
```
cdemu unload 0
```
