# NMGG - A Neural Music Generator GAN

## Usage

Start by cloning this repository:
```
git clone https://github.com/Pasqalup/NMGG.git
```
**Find all DELETE_ME files found in the [notebooks](notebooks/) and delete them**

## Installation
Requires Anaconda or Miniconda<br />

### Create an environment
```
conda create -n NMGG python=3.9
```
### Install Tensorflow
For GPU:
```
conda install -c conda-forge cudatoolkit=11.8.0
python3 -m pip install nvidia-cudnn-cu11==8.6.0.163 tensorflow==2.12.*
mkdir -p $CONDA_PREFIX/etc/conda/activate.d
echo 'CUDNN_PATH=$(dirname $(python -c "import nvidia.cudnn;print(nvidia.cudnn.__file__)"))' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/:$CUDNN_PATH/lib' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
source $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
# Verify install:
python3 -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
```
For CPU:
```
pip install tensorflow-cpu==2.12.*
```
### Install other requirements
```
pip install -r requirements.txt
```
