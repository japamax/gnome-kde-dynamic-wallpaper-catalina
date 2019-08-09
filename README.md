# Gnome time based Catalina wallpaper with real scheludes</br>& KDE Azimuth Elevation based Catalina wallpaper

Catalina dynamic wallpaper is 8 based images wallpaper.</br>
Catalina dynamic wallpaper is useable as Gnome/KDE background which changes during the day/night.</br>
For Gnome, it's a timed based wallpaper with real scheludes with 90 minutes transitions.</br>
For KDE, it's a Azimuth Elevation wallpaper based on real Azimuth Elevation of the Sun for the Catalina island on 21/06/2019.</br></br>


<p align="center">
  <img width="478" height="326" src="gnome-kde-catalina-dynamic-wallpaper.gif">
</p>


# Dependencies
* Gnome
  * gnome-shell
  * gnome-backgrounds
* KDE
  * plasma5-wallpapers-dynamic for Archlinux 
  * or [home: KAMiKAZOW:KDE](https://software.opensuse.org//download.html?project=home%3AKAMiKAZOW%3AKDE&package=plasma5-dynamic-wallpaper) for Opensuze
  - or [GitHub: zzag/dynamic-wallpaper](https://github.com/zzag/dynamic-wallpaper) for others distros

# Parameters
## Gnome
None
## KDE
Select "Dynamic" wallpaper type, put your real coordinates and your timer.


# Installation
## Users of Arch Linux
Arch Linux users  need only clone and build this repository.

```
git clone https://github.com/japamax/gnome-kde-catalina-dynamic-wallpaper.git
cd gnome-kde-catalina-dynamic-wallpaper
makepkg -si
```

## Users of other distros
Users of other distros can manually complete these 5 steps:

1) Copy `catalina` directory from this repo  to `/usr/share/dynamicwallpapers` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/dynamicwallpapers && 
cp -R catalina /usr/share/dynamicwallpapers && 
chmod 755 /usr/share/dynamicwallpapers/catalina && 
chmod 644 /usr/share/dynamicwallpapers/catalina/*
```

2) Link `catalina` directory from `/usr/share/dynamicwallpapers` to `/usr/share/backgrounds/gnome` by running the following as the root user:
```
ln -s /usr/share/dynamicwallpapers/catalina/Images /usr/share/backgrounds/gnome/catalina
```

3) Copy `catalina.json` from this repo  to `/usr/share/dynamicwallpapers/catalina/metadata.json` and make it readable by running the following as the root user:
```
cp catalina.json /usr/share/dynamicwallpapers/catalina/metadata.json && 
chmod 644 /usr/share/dynamicwallpapers/catalina/metadata.json
```

4) Copy `catalina-timed.xml` from this repo  to `/usr/share/backgrounds/gnome` and make it readable by running the following as the root user:
```
cp catalina-timed.xml /usr/share/backgrounds/gnome/catalina-timed.xml && 
chmod 644 /usr/share/backgrounds/gnome/catalina-timed.xml
```

5) Copy `catalina.xml` from this repo  to `/usr/share/gnome-background-properties` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/gnome-background-properties && 
cp catalina.xml /usr/share/gnome-background-properties/catalina.xml && 
chmod 644 /usr/share/gnome-background-properties/catalina.xml
```
