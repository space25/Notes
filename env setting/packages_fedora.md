1. Install apt packages:
    ```
    sudo dnf group install "C Development Tools and Libraries" "Development Tools"
    ```
    ```
    sudo dnf install ufw keepassxc snapd filezilla blender cmake \
    java-latest-openjdk-devel.x86_64 clang boost-devel \
    swig gnome-software flameshot krita openssh-server firefox 
    ```
    ```
    sudo ln -s /var/lib/snapd/snap /snap
    ```
    ```
    flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
    ```
    ```
    sudo snap install blue-recorder
    ```
    or
    ```
    flatpak install flathub com.github.vkohaupt.vokoscreenNG
    ```
2. [Optional] Install QEMU:
    ```
    sudo dnf install @virtualization
    ```
3. Install snap packages
    ```
    sudo snap install pycharm-community --classic &&\
    sudo snap install code --classic &&\
    sudo snap install qtcreator-ros --classic
    ```
