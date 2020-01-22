## Install OpenCV 4.x.x on Ubuntu 18.04 for python 3.7
1. [Install python 3.6 environment](python_environment.md)
1. Update system:
    ```
    sudo apt update -y &&\
    sudo apt upgrade -y &&\
    sudo apt autoremove -y &&\
    sudo apt install -y build-essential cmake git pkg-config\
        libjpeg-dev libtiff-dev  libpng-dev libavcodec-dev\
        libavformat-dev libswscale-dev libv4l-dev\
        libgtk2.0-dev libatlas-base-dev gfortran\
        python-dev python-numpy libtbb2 libtbb-dev\
        libdc1394-22-dev libxvidcore-dev libx264-dev\
        libgtk-3-dev python3-dev python3-numpy\
        libboost-all-dev swig graphviz libgtest-dev\
        doxygen clang qtdeclarative5-dev g++-multilib\
        gcc-multilib texlive-latex-base\
        texlive-fonts-recommended libboost-all-dev netcdf-bin\
        libnetcdf-dev libtool-bin automake ccache\
        qtcreator clang-format default-jdk
    ```
1. Clone repositories:
    ```
    mkdir cv && cd cv &&\
    git clone https://github.com/opencv/opencv_contrib.git &&\
    git clone https://github.com/opencv/opencv.git
    ```
1. Use the [latest stable OpenCV version](https://opencv.org/releases.html):
    ```
    cd opencv_contrib && git checkout <version> && cd .. &&\
    cd opencv && git checkout <version> && cd ..
    ```
1. Activate working environment:
    ```
    source activate <env_name>
    ```
1. Build OpenCV:
    ```
    cd opencv && mkdir build && cd build &&\
    cmake -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D CMAKE_BUILD_TYPE=Release \
    -D BUILD_JPEG=ON \
    -D BUILD_PNG=ON \
    -D BUILD_TIFF=ON \
    -D OPENCV_ENABLE_NONFREE=ON \
    -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules/ \
    -D OPENCV_GENERATE_PKGCONFIG=ON \
    -D WITH_OPENGL=ON \
    -D WITH_TIFF=ON \
    -D BUILD_TIFF=ON \
    -D WITH_OPENGL=ON \
    -D BUILD_opencv_legacy=OFF \
    -D PYTHON3_EXECUTABLE=$(which python3) \
    -D PYTHON_DEFAULT_EXECUTABLE=$(which python3) ..
    ```
    ```
    make -j $(($(nproc))) &&\
    sudo make install &&\
    sudo ldconfig
    ```
1. Check install:
    ```
    ls /usr/local/lib/python3.7/site-packages/
    ```
1. Add links to python env
    ```
    cd /usr/local/lib/python3.7/site-packages/
    ```
    ```
    cd ~/miniconda3/envs/<env_name>/lib/python3.7/site-packages/
    ```
    ```
    ln -s /usr/local/lib/python3.7/site-packages/cv2 cv2
    ```
1. [Configuring Qt Creator](https://github.com/SpaceV2/Notes/blob/master/qtcreator.md)

## Links
1. [Installation in Linux](https://docs.opencv.org/3.1.0/d7/d9f/tutorial_linux_install.html)
2. [OpenCV-C++ Tutorials](https://docs.opencv.org/2.4/doc/tutorials/tutorials.html)
3. [OpenCV-Java Tutorials](http://opencv-java-tutorials.readthedocs.io/en/latest/)
4. [OpenCV-Python Tutorials](https://opencv-python-tutroals.readthedocs.io/en/latest/index.html)
5. [Install OpenCV with OpenCV Contrib](https://github.com/roshanpoudyal/Linux/wiki/Install-OpenCV-with-OpenCV-Contrib-(OpenCV-extra-modules)-on-Linux)
