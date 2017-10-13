## Install OpenCV 3.3 on Ubuntu 16 for python 3.5
1. [Install python 3.5 environment](https://github.com/SpaceV2/Notes/blob/master/python_environment.md)
2. Update system:
    ```
    sudo apt-get update && sudo apt-get upgrade && sudo apt-get autoremove
    ```
3. Install prerequisite libraries:
    ```
    sudo apt-get install build-essential cmake git pkg-config
    ```
4. Install libraries for reading image formats:
    ```
    sudo apt-get install libjpeg-dev libtiff-dev libjasper-dev libpng-dev
    ```
5. Install libraries for reading video formats:
    ```
    sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
    ```
6. Install libraries that allows OpenCV user interface features:
    ```
    sudo apt-get install libgtk2.0-dev
    ```
7. Install libraries that allows us to optimise OpenCV commands:
    ```
    sudo apt-get install libatlas-base-dev gfortran
    ```
8. Optional packages:
    ```
    sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libdc1394-22-dev libxvidcore-dev libx264-dev libgtk-3-dev python3-dev python3-numpy
    ```
9. Clone repositories:
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
10. Build OpenCV:
    ```
    cd opencv && mkdir build && cd build
    ```
    ```
    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D INSTALL_C_EXAMPLES=NO -D INSTALL_PYTHON_EXAMPLES=ON -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules BUILD_EXAMPLES=ON PYTHON3_EXECUTABLE=$(which python3) -D PYTHON_DEFAULT_EXECUTABLE=$(which python3) -D PYTHON3_NUMPY_INCLUDE_DIRS=/usr/lib/python3.5/dist-packages/numpy/core/include/ ..
    ```
    ```
    make -j $(($(nproc)))
    ```
11. Install OpenCV
    ```
    sudo make install
    ```
12. Finish linking dependencies:
    ```
    sudo ldconfig
    ```
13. Check install:
    ```
    ls /usr/local/lib/python3.5/site-packages/
    ```
14. Add links to python env
    ```
    cd /usr/local/lib/python3.5/site-packages/
    ``` 
    ```
    sudo mv cv2.cpython-35m-x86_64-linux-gnu.so cv2.so
    ```
    ```
    cd ~/miniconda3/envs/<env_name>/lib/python3.5/site-packages
    ```
    ```
    ln -s /usr/local/lib/python3.5/site-packages/cv2.so cv2.so
    ```


## Links
1. [Installation in Linux](https://docs.opencv.org/3.1.0/d7/d9f/tutorial_linux_install.html)
2. [OpenCV-C++ Tutorials](https://docs.opencv.org/2.4/doc/tutorials/tutorials.html)
3. [OpenCV-Java Tutorials](http://opencv-java-tutorials.readthedocs.io/en/latest/)
4. [OpenCV-Python Tutorials](https://opencv-python-tutroals.readthedocs.io/en/latest/index.html)