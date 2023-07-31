### Install packages:
```
sudo apt update -y && sudo apt upgrade -y && \
sudo apt install -y git vlc mc filezilla neovim meld firefox \
build-essential cmake default-jdk clang clang-format automake ninja-build g++ gcc gfortran protobuf-compiler libboost-all-dev swig libopencv-dev \
python3 python3-dev python3-pip python3-numpy \
pkg-config libgtk2.0-dev libjpeg-dev libtiff-dev libpng-dev libavcodec-dev
```

### Download and install [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
```
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh && \
bash Miniconda3-latest-Linux-x86_64.sh
```

### Create environment:
```
conda create -n <env_name> python=3.10
```

### Activate environment:
```
conda activate <env_name>
```

### Install libraries:
```
conda install -y scipy numpy matplotlib scikit-learn scikit-image pillow tqdm lxml && \
pip install json5 dotmap numba shapely imagesize opencv-python opencv-contrib-python tensorflow-cpu open3d-cpu && \
conda install -y pytorch torchvision torchaudio cpuonly -c pytorch
```

### Install snap packages
```
sudo snap install pycharm-community --classic &&\
sudo snap install clion --classic &&\
sudo snap install blender --classic
```
