# Installation

We recommend creating a clean *Conda* environment to ensure dependencies don't conflict with your existing Python installations. You will need to have installed or already have mini-conda and git on your system.

## Step 1: Install Mini-conda
Download and install Conda for your operating system, following the instructions. We recommend the Conda distribution [mini-conda](https://docs.anaconda.com/miniconda/)If prompted, add Conda to the PATH variable during installation.

## Step 2: Download and Install u-Unwrap3D repository
Clone the [u-Unwrap3D repository](https://github.com/DanuserLab/u-unwrap3D) onto your system

```
git clone https://github.com/DanuserLab/u-unwrap3D.git
```

## Step 3: Create Conda environment for u-Unwrap3D
Open a terminal or command prompt in the root folder of the u-Unwrap3D repository. Create and activate a new conda environment with Python=3.9. Later versions should also work. 

```
conda create -n u_Unwrap3D_env python=3.9
conda activate u_Unwrap3D_env
```

## Step 4: Install u-Unwrap3D from cloned repository
Perform `pip install` in the root folder of the u-Unwrap3D repository

```
pip install .
```

alternatively, if you don't want to clone you can use `pip` to also install the package directly without cloning from the github repository.

```
pip install u-unwrap3D@git+https://github.com/DanuserLab/u-unwrap3D.git
```

### Known Installation Issues 
- `scikit-fmm` compilation error
The `scikit-fmm` dependency does not have pre-compiled wheels available in `pip`. This can create an error for operating systems without the necessary compilation tools installed. It is a minor dependency, therefore either remove this from the file `requirements.txt`, if you have cloned the repository or install `scikit-fmm` first using `conda` using the `conda-forge` channel:
```
conda install -c conda-forge scikit-fmm
```