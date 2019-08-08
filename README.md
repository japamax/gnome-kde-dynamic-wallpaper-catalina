# Gnome time based catalina wallpaper with real scheludes

Catalina dynamic wallpaper useable as gnome background which changes during the day/night. 
Real scheludes with twenty minutes transitions.

<p align="center">
  <img width="478" height="326" src="gnome-kde-catalina-dynamic-wallpaper.gif">
</p>

# Dependencies
* gnome-shell
* gnome-backgrounds

# Installation
## Users of Arch Linux
Arch Linux users  need only clone and build this repository.

```
git clone https://github.com/japamax/gnome-catalina-timed-wallpaper.git
cd gnome-catalina-timed-wallpaper
makepkg -si
```

## Users of other distros
Users of other distros can manually complete these 3 steps:

1) Copy `catalina` directory from this repo  to `/usr/share/backgrounds/gnome` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/backgrounds/gnome && 
cp -R catalina /usr/share/backgrounds/gnome && 
chmod 755 /usr/share/backgrounds/gnome/catalina && 
chmod 644 /usr/share/backgrounds/gnome/catalina/*
```

2) Copy `catalina-timed.xml` from this repo  to `/usr/share/backgrounds/gnome` and make it readable by running the following as the root user:
```
cp catalina-timed.xml /usr/share/backgrounds/gnome/catalina-timed.xml && 
chmod 644 /usr/share/backgrounds/gnome/catalina-timed.xml
```

3) Copy `catalina.xml` from this repo  to `/usr/share/gnome-background-properties` and make it readable by running the following as the root user:
```
mkdir -p /usr/share/gnome-background-properties && 
cp catalina.xml /usr/share/gnome-background-properties/catalina.xml && 
chmod 644 /usr/share/gnome-background-properties/catalina.xml
```
