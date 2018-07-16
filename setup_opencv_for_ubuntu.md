## Install OpenCV 3.4 on Ubuntu 18.04 for python 3.6
1. [Install python 3.6 environment](https://github.com/SpaceV2/Notes/blob/master/python_environment.md)
1. Update system:
    ```
    sudo apt update && sudo apt upgrade && sudo apt autoremove
    ```
1. Install prerequisite libraries:
    ```
    sudo apt install build-essential cmake git pkg-config
    ```
1. Install libraries for reading image formats:
    ```
    sudo apt install libjpeg-dev libtiff-dev  libpng-dev
    ```
1. Install libraries for reading video formats:
    ```
    sudo apt install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
    ```
1. Install libraries that allows OpenCV user interface features:
    ```
    sudo apt install libgtk2.0-dev
    ```
1. Install libraries that allows us to optimise OpenCV commands:
    ```
    sudo apt install libatlas-base-dev gfortran
    ```
1. Optional packages:
    ```
    sudo apt install python-dev python-numpy libtbb2 libtbb-dev\
                         libdc1394-22-dev libxvidcore-dev libx264-dev\
                         libgtk-3-dev python3-dev python3-numpy\
                         libboost-all-dev swig graphviz libgtest-dev\
                         doxygen clang qtdeclarative5-dev g++-multilib\
                         gcc-multilib texlive-latex-base exlive-latex-extra\ texlive-fonts-recommended libboost-all-dev netcdf-bin\
                         libnetcdf-dev libtool-bin automake ccache
    ```
1. Clone repositories:
    ```
    git clone https://github.com/Itseez/opencv_contrib.git
    ```
    ```
    cd opencv_contrib && git checkout <version> && cd ..
    ```
    ```
    git clone https://github.com/Itseez/opencv.git
    ```
    ```
    cd opencv && git checkout <version> && cd ..
    ```
1. Activate working environment:
    ```
    source activate <env_name>
    ```
1. Build OpenCV:
    ```
    cd opencv && mkdir build && cd build
    ```
    ```
    cmake -D CMAKE_BUILD_TYPE=RELEASE \
        -D CMAKE_INSTALL_PREFIX=/usr/local \
        -D INSTALL_C_EXAMPLES=OFF \
        -D INSTALL_PYTHON_EXAMPLES=OFF \
        -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules \
        -D BUILD_opencv_legacy=OFF \
        -D BUILD_EXAMPLES=OFF\
        -D PYTHON3_EXECUTABLE=$(which python3) \
        -D PYTHON_DEFAULT_EXECUTABLE=$(which python3) \
        -D WITH_CUDA=OFF \
        -D WITH_OPENGL=ON \
        -D WITH_TIFF=ON \
        -D BUILD_TIFF=ON \
        -D PYTHON3_NUMPY_INCLUDE_DIRS=/usr/lib/python3/dist-packages/numpy/core/include/ ..
    ```
    ```
    make -j $(($(nproc)))
    ```
1. Install OpenCV
    ```
    sudo make install
    ```
1. Finish linking dependencies:
    ```
    sudo ldconfig
    ```
1. Check install:
    ```
    ls /usr/local/lib/python3.6/site-packages/
    ```
1. Add links to python env
    ```
    cd /usr/local/lib/python3.6/site-packages/
    ```
    ```
    sudo ln -s cv2.cpython-36m-x86_64-linux-gnu.so cv2.so
    ```
    ```
    cd ~/miniconda3/envs/<env_name>/lib/python3.6/site-packages/
    ```
    ```
    ln -s /usr/local/lib/python3.6/site-packages/cv2.so cv2.so
    ```


## Links
1. [Installation in Linux](https://docs.opencv.org/3.1.0/d7/d9f/tutorial_linux_install.html)
2. [OpenCV-C++ Tutorials](https://docs.opencv.org/2.4/doc/tutorials/tutorials.html)
3. [OpenCV-Java Tutorials](http://opencv-java-tutorials.readthedocs.io/en/latest/)
4. [OpenCV-Python Tutorials](https://opencv-python-tutroals.readthedocs.io/en/latest/index.html)
