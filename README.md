# Pytorch Examples
This repository shows basic code examples of the pytorch.

## Table of contents
### 1. Pytorch Basic
- Basic Operations [[ipynb]](notebooks/1_PytorchBasic/BasicOperation.ipynb)

### 2. DataLoader
- Description of DataLoader / Sampler [[ipynb]]()

### 3. MLP
- Classification of the MNIST Dataset [[ipynb]](notebooks/3_MLP/MLP_MNIST.ipynb)

### 4. Convolutional Neural Network
- Classification of the MNIST Dataset using CNN [[ipynb]]()

### 5. Sequence Models
- Simple Text Generation using RNN [[ipynb]]()
- Sequence Text Generation using LSTM [[ipynb]]()

### 6. Transformer
T.B.D.

### 7. Vision Transformer
T.B.D.

## Environment
- Preconditions
    - Install Docker >= 19.03
    - Install Nvidia Driver >= 520
    - Install Nvidia Container Toolkit
        - https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#docker
    - Setup access right to NVIDIA NGC

- Build dockerfile
    ```bash
    $ cd Docker
    $ docker build -t pytorch-examples:latest .
    ```

- Run container
    ```bash
    $ docker run --gpus all -it --rm -v {local_dir}:/home/developer/workspace -p 8888:8888 --ipc=host --shm-size=16g --ulimit memlock=-1 --ulimit stack=67108864 pytorch-examples:latest
    ```

- Activate Jupyter Notebook
    ```bash
    $ jupyter notebook -ip=0.0.0.0
    ```

