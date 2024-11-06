To use this repo, clone it using

git clone git@github.com:ericcropp/NERSC_Impact-T_Example.git

Then, to get the submodules to load:

git submodule update --init --recursive

Finally, to set up the conda environment on NERSC:

1) Navigate to the directory above
2) conda env create -f environment.yml
3) Follow these instructions: https://docs.nersc.gov/services/jupyter/how-to-guides/#how-to-use-a-conda-environment-as-a-python-kernel
    a) conda activate Multifidelity
    b) python -m ipykernel install --user --name env --display-name MyEnvironment
4) Go to jupyter.nersc.gov, initiate a session ON A CPU EXCLUSIVE NODE (if you want to use parallel processing), and select a kernel

The components of this library are as follows:
1) VCC_March_2024.jpeg: VCC image for Distgen
2) environment.yml: a list of packages needed to recreate the conda environmnet
3) distgen.yaml: Input file for Distgen (a distribution generator)
4) Example.ipynb: The example notebook.  
5) ImpactT-template.yaml: Input file for Impact-T (Distgen output is fed into Impact-T)