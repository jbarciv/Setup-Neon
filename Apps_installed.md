# Applications installed and commands 
## Installation instructions by programms
### Kate

```
sudo apt-get update
sudo apt-get install kate
```
### Google Chrome
For Kde Neon it is recommended this:
```
wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt-get update
sudo apt-get install libappindicator1
sudo dpkg -i google-chrome-stable_current_amd64.deb
```
For Ubuntu 20.04 olmost the same:
```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
```

### VSCode
```
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
```
### Assign Meta key to Dashboard (Windows key for app menu)
Here we present three options:
1) Make sure that the following lines are included in the `kwinrc` text file in the `~/.config` directory:
```
[ModifierOnlyShortcuts]
Meta=org.kde.lattedock,/Latte,org.kde.LatteDock,activateLauncherMenu
```
Then, map the applet activation key to `Meta + F1` or `Alt + F1`.

2) If this method does not work, check out [this](https://askubuntu.com/a/246953/1166016) StackOverflow answer.

3) Also, you can assign *meta*+*A* as a shortcut for Application Dashboard and then assign the *meta* key to that shortcut (typing the next lines on terminal). 
```
sudo apt install xcape
xcape -e 'Super_L=Super_L|A'
```
4) Finally, for Latte-Dock users, there is an option (right click on the Dock) in *Configure Latte..*. Check the box: *Press Meta to activate Application Launcher*.

### WPS Office 2019 Multi-Languague
Open the snap store app and search wps. Install `WPS Office 2019 Multi-Language`.
Or type this on your terminal:
```
sudo snap install wps-2019-snap
```
Post installation configuration:
```
sudo snap connect wps-2019-snap:cups-control :cups-control
sudo snap connect wps-2019-snap:alsa :alsa
sudo snap connect wps-2019-snap:pulseaudio :pulseaudio
sudo snap connect wps-2019-snap:removable-media :removable-media
```

### Inkscape
```
sudo apt-get update -y
sudo apt-get install inkscape
```

### indicator-stickynotes
See [this](https://launchpad.net/~umang/+archive/ubuntu/indicator-stickynotes) for more information.
```
sudo apt-add-repository ppa:umang/indicator-stickynotes
sudo apt-get update && sudo apt-get install indicator-stickynotes
```

### Latex and Kile
See [this](https://linuxconfig.org/how-to-install-latex-on-ubuntu-20-04-focal-fossa-linux) fore other installation options.
```
sudo apt-get install texlive
sudo apt install kile
```

### PDF-Shuffler
```
sudo add-apt-repository ppa:pdfshuffler/ppa
sudo apt-get update
sudo apt-get install pdfshuffler
```

### Flameshot
```
sudo apt-get install flameshot
```
For running from terminal: `flameshot gui -p /home/your/desired/directory`. I highly recommend you creating a shortcut with this.

## Installation instructions (all together)

```
echo Installing Kate editor
sudo apt-get update
sudo apt-get install kate

echo Installing Google Chrome and some libraries
wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt-get update
sudo apt-get install libappindicator1
sudo dpkg -i google-chrome-stable_current_amd64.deb

echo Installing VSCode
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code

echo Installing WPS Office 2019
sudo snap install wps-2019-snap
sudo snap connect wps-2019-snap:cups-control :cups-control
sudo snap connect wps-2019-snap:alsa :alsa
sudo snap connect wps-2019-snap:pulseaudio :pulseaudio
sudo snap connect wps-2019-snap:removable-media :removable-media

echo Installing Inkscape
sudo apt-get install inkscape

echo Installing Sticky Notes
sudo apt-add-repository ppa:umang/indicator-stickynotes
sudo apt-get update && sudo apt-get install indicator-stickynotes

echo Installing Latex and Kile
sudo apt-get install texlive
sudo apt install kile

echo Installing PDF-Shuffler
sudo add-apt-repository ppa:pdfshuffler/ppa
sudo apt-get update
sudo apt-get install pdfshuffler
```

## Other tricks
### Desktop file and Icons
Example of desktop file:
```
[Desktop Entry]
Encoding=UTF-8
Version=1.0
Type=Application
Terminal=false
Exec=/usr/bin/ipe
Name=Ipe
Icon=/usr/share/ipe/7.2.23/icons/icon_128x128.png
```
Application drawer is: `/usr/share/applications`:applications shown with meta in kde
