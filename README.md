
This temporary repository provides all code, data, and scripts for the experiments in the paper `Semi-Implicit Neural Ordinary Differential Equations`. Data files larger than 100MB are not included because of the repo limitation.

---

## Installation
petsc4py needs to be installed first. The suggested way to install petsc4py is to install it from PETSc source
```
git clone https://gitlab.com/petsc/petsc.git
cd petsc
./configure PETSC_ARCH=arch-linux-opt --with-debugging=0 --download-petsc4py
```
Here minimal configure options are provided. Several other widely used options are listed below:

 - `--with-cude=1` Use CUDA if an NVIDIA GPU is available.
 - `--with-fc=0` Disable Fortran if you do not have a Fortran compiler or do not need Fortran.
 - `--with-precision=single` Build PETSc with single precision (without his option, PETSc uses double precision).
Note that `PETSC_ARCH` takes of your choice. One can create many different versions of PETSc, each of which can have a different list of options and be given a different name specified by `PETSC_ARCH`.

After configure, follow the instructions on screen to do make all and make check (optional).

After petsc4py is installed, install PNODE
```
cd pnode
pip3 install .
```

