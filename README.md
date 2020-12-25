Use tensorflow 2.1.2 and Cuda 10.1
For Cuda install see https://medium.com/@exesse/cuda-10-1-installation-on-ubuntu-18-04-lts-d04f89287130

```
sudo rm /etc/apt/sources.list.d/cuda*
sudo apt remove --autoremove nvidia-cuda-toolkit
sudo apt remove --autoremove nvidia-*
```

```
sudo apt update
sudo add-apt-repository ppa:graphics-driverssudo apt-key adv --fetch-keys  http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pubsudo bash -c 'echo "deb http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda.list'sudo bash -c 'echo "deb http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda_learn.list'
```

```
sudo apt update
sudo apt install cuda-10-1
sudo apt install libcudnn7
```

```
pip install -U pip
pip install -U setuptools
```


![version](https://img.shields.io/github/manifest-json/v/linto-ai/hmg)

# Hotword Model Generator
HMG is a GUI tool designed to generate keyword spotting models.

**DISCLAIMER: This is an rough version of a tool that haven't beed thoroughly tested, bug may (and probably will) occur. Please use the issue tracker to report them.**

## Introduction
HMG allows you to:
* Manage data
* Tune audio features
* Tune model architecture and training parameters
* Train your model
* Evaluate your model
* Test your model
* Export your model
__________________
## Getting Started
There are 2 options to use this software:
* Using the binary release.
* Cloning this repository

### Release

**Release version: Unavailable** 

Binary have been generated using PyInstaller on Ubuntu 18.04.
You can download the lastest release [there](https://github.com/linto-ai/hmg/releases/download/0.3/hmg-v0.3-ubuntu.tar.gz).

1. Extract the archive
```bash
tar xzf $(ARCHIVE)
```
A ```hmg/``` folder shall be extracted.

2. Launch the program
```bash
./hmg/hmg
```
### From Source
You can use the software from the repository.

**Prerequisites**

You need ```python3.x``` and ```python3-pip``` installed.

There is a number of dependencies needed to run the software.
They can be found in the ```requirements.txt``` file at the repository root.

We recommend that you use a virtual environement.
```bash
source /my/virtual/env/bin/activate #Optionnal but advised
cd $(REPO_ROOT)
pip install -r requirements.txt
```

You can launch the program by running either:
```bash
python $(REPO_ROOT)/model_generator/main.py
# or
./$(REPO_ROOT)/model_generator/main.py
```
__________________
## Usage
See the [documentation](https://doc.linto.ai/#/client/custom_hotword)
__________________
## Built using

* [Qt](https://www.qt.io/) - Cross-platform software development for embedded GUI
* [PyQt](https://riverbankcomputing.com/software/pyqt/intro) - Python binding for Qt
* [Tensorflow](https://www.tensorflow.org) - An open source machine learning library for research and production

__________________
## License
This project is licensed under the GNU AFFERO License - see the [LICENSE.md](LICENSE.md) file for details.
