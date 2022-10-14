1. Install apt packages:
  ```
  sudo dnf install ufw keepassxc snapd filezilla blender \
  snapd build-essential cmake default-jdk clang clang-format automake ninja-build \
  g++ gcc gfortran protobuf-compiler libboost-all-dev swig flameshot kazam krita openssh-server firefox
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
