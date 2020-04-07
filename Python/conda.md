# Common Anaconda Commands

```bash
# To create an environment call this command:
conda create --name environment_name python=3.7
# You can save all the info necessary to recreate the environment in a file by calling
conda env export > environment.yml
# To recreate the environment you can do the following:
conda env create -f environment.yml

# Start out
conda deactivate
conda activate environment_name
# list all installed packages
conda list
# list all current environments
conda env list

```