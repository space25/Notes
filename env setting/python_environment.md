## Setup Python 3.7 environment for Ubuntu 20.04:
1. Download and install [Miniconda](https://conda.io/miniconda.html)
    ```
    wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh && \
    bash Miniconda3-latest-Linux-x86_64.sh
    ```
1. Create environment:
    ```
     conda create -n <env_name> python=3.7
    ```
1. Activate environment:
    ```
    conda activate <env_name>
    ```
1. Install dependency:
    ```
    conda install -y scipy numpy matplotlib scikit-learn scikit-image pillow tqdm lxml && \
    pip install json5 dotmap numba shapely imagesize opencv-python opencv-contrib-python && \
    conda install -y pytorch torchvision cpuonly -c pytorch && \
    pip install tensorflow-cpu
    ```
1. [Install PyCharm](https://www.jetbrains.com/pycharm/download/#section=linux)
    ```
    sudo snap install pycharm-community --classic
    ```
