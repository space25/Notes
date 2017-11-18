FROM tensorflow/tensorflow:1.4.0-gpu-py3

RUN apt-get update -y && apt-get upgrade -y && apt-get autoremove &&\
    apt-get install -y curl wget nano python3-tk

RUN apt-get install -y build-essential cmake git pkg-config\ 
    libjpeg-dev libtiff-dev libjasper-dev libpng-dev\
    libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libgtk2.0-dev\
    libatlas-base-dev gfortran libtbb2 libtbb-dev\
    libdc1394-22-dev libxvidcore-dev libx264-dev libgtk-3-dev python3-dev python3-numpy\
    python-dev python-numpy protobuf-compiler python-pil python-lxml

RUN pip --no-cache-dir install scipy numpy matplotlib scikit-learn scikit-image\
    csvkit jupyter numexpr cloudpickle pickleshare h5py hdf5storage CFFI Pillow tqdm

RUN mkdir cv && cd cv && git clone https://github.com/Itseez/opencv_contrib.git &&\
    git clone https://github.com/Itseez/opencv.git

RUN cd cv/opencv_contrib &&\
    git checkout 3.3.1 &&\
    cd .. && cd opencv &&\
    git checkout 3.3.1 &&\
    mkdir build

RUN cd cv/opencv/build && cmake\
    -D CMAKE_BUILD_TYPE=RELEASE\
    -D CMAKE_INSTALL_PREFIX=/usr/local\
    -D INSTALL_C_EXAMPLES=OFF\
    -D INSTALL_PYTHON_EXAMPLES=OFF\
    -D OPENCV_EXTRA_MODULES_PATH=/notebooks/cv/opencv_contrib/modules\
    -D BUILD_opencv_legacy=OFF\
    -D BUILD_EXAMPLES=OFF\
    -D PYTHON3_EXECUTABLE=$(which python3)\
    -D PYTHON_DEFAULT_EXECUTABLE=$(which python3)\
    -DENABLE_AVX=ON \
    -DWITH_IPP=ON \
    -DWITH_TBB=ON \
    -DWITH_EIGEN=ON \
    -DWITH_V4L=ON \
    -DWITH_GTK=ON \
    -DWITH_GTK_2_X=ON \
    -D PYTHON3_NUMPY_INCLUDE_DIRS=/usr/lib/python3.5/dist-packages/numpy/core/include/ ..

RUN cd cv/opencv/build make -j 4 && make install && ldconfig && rm -rf cv

RUN cd /usr/local/lib/python3.5/dist-packages &&\
    ln -s cv2.cpython-35m-x86_64-linux-gnu.so cv2.so

RUN apt-get clean 
# RUN rm -rf /var/lib/apt/lists/*

WORKDIR "/root"
