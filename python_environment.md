## Setup Python 3.6 environment for Ubuntu 16.04:
1. Download and install [Miniconda](https://conda.io/miniconda.html)
    ```
    wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh && \
    bash Miniconda3-latest-Linux-x86_64.sh
    ```
1. Create environment:
    ```
     conda create -n <env_name> python=3.6
    ```
1. Activate environment:
    ```
    source activate <env_name>
    ```
1. Install dependency:
    ```
    conda install -y scipy numpy matplotlib scikit-learn scikit-image csvkit jupyter \
    nomkl numexpr cloudpickle pickleshare h5py CFFI requests beautifulsoup4 line_profiler \
    memory_profiler pillow tqdm lxml && \
    pip install xgboost editdistance cairocffi
    ```
1. [optional] Check env using jupyter:
    ```
    jupyter notebook --notebook-dir=<project_dir>
    ```
1. [Install TensorFlow on Ubuntu](https://www.tensorflow.org/install/install_linux#InstallingAnaconda)
1. [Install OpenCV](Setup_OpenCV_for_Ubuntu_16.md)
1. [Install PyCharm](https://www.jetbrains.com/pycharm/download/#section=linux)
