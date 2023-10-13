1. Install apt packages:
    ```
    sudo apt install -y git terminator vlc mc filezilla neovim meld \
    build-essential cmake default-jdk clang clang-format automake ninja-build g++ gcc gfortran protobuf-compiler libboost-all-dev swig libopencv-dev \
    python3 python3-dev python3-pip python3-numpy \
    pkg-config libgtk2.0-dev libjpeg-dev libtiff-dev libpng-dev libavcodec-dev libffi-dev
    ```
    [optional]
    ```
    sudo apt install -y gnome-boxes
    sudo apt install -y gnome-tweaks
    sudo apt install -y gnome-software
    sudo apt install -y ubuntu-restricted-extras
    ```
    
    [optional]
    ```
    sudo apt --only-upgrade install <Package>
    ```
    [optional]
    ```
    snap refresh --list
    ```
    ```
    snap refresh
    ```
    
1. [Optional] Install QEMU:
    ```
    sudo apt install -y qemu-kvm bridge-utils libvirt-daemon virt-manager \
	libvirt-clients libvirt-daemon-system
    ```
    ```
    sudo adduser $USER libvirt
    ```
    or
    ```
    sudo usermod -aG libvirt $USER
    ```

1. Install snap packages
    ```
    sudo snap install docker &&\
    sudo snap install pycharm-community --classic &&\
    sudo snap install code --classic &&\
    sudo snap install qtcreator-ros --classic &&\
    sudo snap install opera &&\
    sudo snap install keepassxc &&\
    sudo snap install blender --classic
    ```
1. How To Fix System Program Problem Detected In Ubuntu
    ```
    sudo rm /var/crash/*
    ```
1. Install tools
    ```
    sudo snap install clion --classic &&\
    sudo snap install pycharm-community --classic &&\
    sudo snap install gedit &&\
    sudo apt install eog
    ```
