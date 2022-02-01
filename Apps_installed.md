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
