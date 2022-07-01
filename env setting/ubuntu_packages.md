1. Install apt packages:
    ```
    sudo apt install -y git terminator vlc mc filezilla neovim meld \
    build-essential cmake default-jdk clang clang-format automake ninja-build g++ gcc gfortran protobuf-compiler libboost-all-dev \
    libopencv-dev libpcl-dev \
    flameshot kazam krita openssh-server
    ```
    [optional]
    ```
    sudo apt install -y gnome-tweaks
    sudo apt install -y gnome-software
    sudo apt install -y ubuntu-restricted-extras
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
    sudo snap install blender --classic
    ```
1. How To Fix System Program Problem Detected In Ubuntu
    ```
    sudo rm /var/crash/*
    ```
