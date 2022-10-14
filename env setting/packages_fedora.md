1. Install apt packages:
    ```
    sudo dnf group install "C Development Tools and Libraries" "Development Tools"
    ```
    ```
    sudo dnf install ufw keepassxc snapd filezilla blender snapd \
    java-latest-openjdk-devel.x86_64 clang boost-devel swig flameshot krita openssh-server firefox
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
