# Applications installed and commands 
## Installation instructions by programms
### Kate

```
sudo apt-get update
sudo apt-get install kate
```
### Google Chrome
```
wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt-get update
sudo apt-get install libappindicator1
sudo dpkg -i google-chrome-stable_current_amd64.deb
```
### VSCode
```
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
```
### Assign Meta key to Dashboard
```
sudo apt install xcape
xcape -e 'Super_L=Super_L|A'
```

### WPS Office 2019 Multi-Languague
Open the snap store app and search wps. Install `WPS Office 2019 Multi-Language`.
Or type this on your terminal:
```
sudo snap install wps-2019-snap
sudo snap connect wps-office-multilang:removable-media
```
Post installation configuration:
```
sudo snap connect wps-2019-snap:cups-control :cups-control
sudo snap connect wps-2019-snap:alsa :alsa
sudo snap connect wps-2019-snap:pulseaudio :pulseaudio
sudo snap connect wps-2019-snap:removable-media :removable-media
```

## Installation instructions (all together)

```
sudo apt-get update
sudo apt-get install kate

wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt-get update
sudo apt-get install libappindicator1
sudo dpkg -i google-chrome-stable_current_amd64.deb

sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
```
