RU Proverbs AI module
-------
[![PyPI version](https://badge.fury.io/py/ru-proverbs.svg)](https://badge.fury.io/py/ru-proverbs)

This module provides API that allows to generate Russian Proverbs with the power of AI.

# Requirements
 
For Windows builds:

In the current version we use Python 3.7.6, Tensorflow 2.1 and CUDA 10.1.

1. Python 3.7.x. x64 (tested with [Python 3.7.6x64][python]).

2. Properly installed [Tensorflow][tensorflow] inside the virtual env:
    
    2.1 Install virtual env: `python -m venv .venv`.
    
    2.2 Upgrade pip: `python -m pip install --upgrade pip`.
    
    2.3 Upgrade setuptools: `pip install --upgrade setuptools`.
    
    2.3 Install Tensorflow: `pip install --upgrade tensorflow`
    
    2.4 Optionally install and configure CUDA support.
    
3. Install other requirements: `pip install --upgrade -r requirements.txt`

## Configure CUDA

1. Download [CUDA Toolkit][cuda-toolkit] and unpack into e.g. `D:\DevTools\cuda\v10.1`.

2. Download matching [cuDNN][cuDNN] version (e.g. v7.6.5 for CUDA 10.1) and unpack
under the versioned CUDA folder, e.g. `D:\DevTools\cuda\v10.1\cudnn`.

3. Add CUDA paths to environment variables and `PATH`:
    
    Create `CUDA_HOME` and `CUDA_PATHS` env variables with the following values:
    ```cmd
    SET CUDA_HOME=D:\DevTools\cuda\v10.1
    SET CUDA_PATHS=%CUDA_HOME%\bin;%CUDA_HOME%\include;%CUDA_HOME%\extras;%CUDA_HOME%\libnvvp;%CUDA_HOME%\cudnn\bin;
    ```
    
    Add `CUDA_PATHS` to `PATH`: `SET PATH=%CUDA_PATHS%;%PATH%`.

 

[python]: https://www.python.org/downloads/release/python-376/
[tensorflow]: https://www.tensorflow.org/install/pip
[cuda-toolkit]: https://developer.nvidia.com/cuda-10.1-download-archive-update2?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exelocal
[cuDNN]: https://developer.nvidia.com/rdp/cudnn-download