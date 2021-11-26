# Apple M1 / M1 Pro / M1 Max GPU Training Example

This repository provides instruction to install proper TensorFlow version for Apple M1/M1 Pro/M1 Max processors and train with M1 GPUs.

## Install TensorFlow on M1 / M1 Pro / M1 Max machine

The typical procedures to install Tensowflow such as pip or native ways do not work on M1 machines due to having h5py dependency. The following way is to install TF on M1 machines with GPU performance:

### Install Miniforge for OS X Apple Silicon

[How to install Miniforge on Apple Silicon machine](https://github.com/conda-forge/miniforge)

* `conda config --set auto_activate_base false` to deactivate default base env from miniforge.

### Create a conda environment and activate it

* `conda create --name [ENV NAME] python=[PYTHON VERSION PREFERABLY >=3.8]`

* `conda activate [ENV NAME]`

### Install TensorFlow>=2.6.0 for Mac OS

* `conda install -c apple tensorflow-deps` for dependencies.

* `pip install tensorflow-macos` for base TF version.

* `pip install tensorflow-metal` for TF with Metal support.

### Install Jupyter Notebook

* `conda install -c conda-forge -y jupyter`

## Install Requirements

pip install -r requirements.txt

## Run the classifier example Python script

python src/classifier.py

## Run the classifier example in Jupyter Notebook

src/classifier.ipynb

## References

* [How To Install TensorFlow on M1 Mac (The Easy Way)](https://caffeinedev.medium.com/how-to-install-tensorflow-on-m1-mac-8e9b91d93706)

* [TensorFlow for Mac OS](https://www.tensorflow.org/install/mac)

* [Miniforge](https://github.com/conda-forge/miniforge)
