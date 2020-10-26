# workshopDataWrangling

#Download GeneRIFs Database

https://uchicago.box.com/s/3018iv1tyz1bcx5zmvpfr3frc6jbxepi

#transfer file from your local folder to the server

scp filename CNETID@midway2.rcc.uchicago.edu:/PATH/TO/FOLDER
  
scp : secure copy.  

Steps to create your own conda environment at RCC cluster

You can use your scratch or project space. Home space is not recommended because it has limited space. 

https://rcc.uchicago.edu/docs/data-storage/index.html

First load anaconda module

module load python/anaconda-2020.02

 Create conda environment :
 
conda create --name [env_name] --prefix /scratch/midway2/[cnetid]/[env_name]

Activate conda environment:

conda activate  /scratch/midway2/[cnetid]/[env_name]

To install conda packages, in the terminal type

conda install

Install Jupyter lab using conda

conda has many channels (locations where packages are stored) so we will use conda-forge as an example( --channel or  -c conda-forge)

conda install -c conda-forge jupyterlab

Install IRkernel  

module load python/anaconda-2020.02

module load R/3.6.1

conda activate /scratch/midway2/humaasif/conda-env # change according to your Path

R : command line interface

Type R in terminal

Next to > symbol, type

Install.packages((“IRkernel”)

For making the kernel available to Jupyter,  type this command in R:

IRkernel::installspec()

To check all jupyter kernel installed

jupyter kernelspec list

To deactivate conda

conda deactivate

To run the jupyter Notebook script, first modify these lines


TIME="04:00:00" # Set walltime

MEM="32GB" # set memory

N_CPU=1. # set number of CPUs

PART=edu


PYTHON_MODULE="anaconda-2020.02"  # Python module to use anaconda dist of python

CONDA_ENV="/scratch/midway2/humaasif/conda-env"    # change conda environment name. 

R_HOME="R/3.6.1"   



LOGS="/home/humaasif/WorkshopMaterial" # change this according to your folder
          

