wsl -l -v

wsl --set-default-version <Version#>

wsl --set-version <distro name> 2
  
wsl --unregister <distro name>
  
wsl --shutdown
  

sudo apt update && sudo apt upgrade && sudo apt install gedit gimp nautilus vlc x11-apps

## Google Chrome
cd /tmp && \
sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && \
sudo dpkg -i google-chrome-stable_current_amd64.deb && \
sudo apt install --fix-broken -y && \
sudo dpkg -i google-chrome-stable_current_amd64.deb

## Links
* https://github.com/microsoft/wslg
* https://learn.microsoft.com/ru-ru/windows/wsl/install
* https://www.youtube.com/playlist?list=PLhfrWIlLOoKNMHhB39bh3XBpoLxV3f0V9
* https://www.windowscentral.com/how-completely-remove-linux-distro-wsl
* https://forum.snapcraft.io/t/running-snaps-on-wsl2-insiders-only-for-now/13033
