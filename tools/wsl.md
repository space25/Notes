### [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
(Open PowerShell or Windows Command Prompt in administrator mode):
```
  wsl --install
```

### Main commands:
```
  wsl -l -v
  wsl --set-default-version <Version#>
  wsl --set-version <distro name> 2
  wsl --unregister <distro name>  
  wsl --shutdown
```

### Install image:
```
wsl --list --online
```
```
wsl --install -d <Distro>
```

### Remove a Linux distro:
```
wsl --list
```
```
wsl --unregister <DISTRO-NAME>
```
  
### Update system:
```
  sudo apt update && sudo apt upgrade
```

### Enable systemd:
```
wsl --update
```
Add these lines to the /etc/wsl.conf:
```
sudo nano /etc/wsl.conf
```
```
[boot]
systemd=true

[user]
default=DemoUser
```

### Multiple WSL distro instances:
```
wsl --help
```
```
wsl --export <Distro> <FileName> # wsl --export Ubuntu D:\wsl\ubuntu.tar
```
```
wsl --import <Distro> <InstallLocation> <FileName>
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

### [optionally] Install [MobaXterm](https://mobaxterm.mobatek.net/) or [mRemoteNG](https://mremoteng.org/)

## Links
* [Systemd support is now available in WSL!](https://devblogs.microsoft.com/commandline/systemd-support-is-now-available-in-wsl/)
* [How to completely remove a Linux distro from the Windows Subsystem for Linux (WSL)](https://www.windowscentral.com/how-completely-remove-linux-distro-wsl)
* https://github.com/microsoft/WSL/releases
* https://learn.microsoft.com/en-us/windows/wsl/install
* https://github.com/microsoft/wslg
* https://www.youtube.com/playlist?list=PLhfrWIlLOoKNMHhB39bh3XBpoLxV3f0V9
* https://www.windowscentral.com/how-completely-remove-linux-distro-wsl
* https://forum.snapcraft.io/t/running-snaps-on-wsl2-insiders-only-for-now/13033
