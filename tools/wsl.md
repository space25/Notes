### Main commands:
```
  wsl -l -v
  wsl --set-default-version <Version#>
  wsl --set-version <distro name> 2
  wsl --unregister <distro name>  
  wsl --shutdown
```
  
### Update system:
```
  sudo apt update && sudo apt upgrade
```
  
### Install basic libraries:
```
  sudo apt install -y gedit gimp nautilus vlc x11-apps curl wget 
```
  
### Install dev libraries:
```
  sudo apt install -y git terminator vlc mc filezilla neovim meld tar zip rsync \
  build-essential cmake default-jdk clang clang-format automake ninja-build g++ gcc gfortran protobuf-compiler \
  libopencv-dev libboost-all-dev swig libjsoncpp-dev libgtk2.0-dev pkg-config libjpeg-dev libtiff-dev libpng-dev libavcodec-dev \
  python3 python3-dev python3-pip python3-numpy
```

### Install Google Chrome:
```
  cd /tmp && \
  sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && \
  sudo dpkg -i google-chrome-stable_current_amd64.deb && \
  sudo apt install --fix-broken -y && \
  sudo dpkg -i google-chrome-stable_current_amd64.deb
```
  
### Install Brave browser:
```
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg &&\
echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list &&\
sudo apt update &&\
sudo apt install brave-browser
```

## Links
* https://github.com/microsoft/wslg
* https://learn.microsoft.com/ru-ru/windows/wsl/install
* https://www.youtube.com/playlist?list=PLhfrWIlLOoKNMHhB39bh3XBpoLxV3f0V9
* https://www.windowscentral.com/how-completely-remove-linux-distro-wsl
* https://forum.snapcraft.io/t/running-snaps-on-wsl2-insiders-only-for-now/13033
