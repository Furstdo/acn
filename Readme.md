# ACN

## Installation overview

1. clone repository from GitHub
1. create conda environment
1. setup secret in ```.env``` file

### GitHub Clone

Clone this repository with Visual Studio Code into your home directory.  
Open the directory afterwards as new window. Use the following URL  

```
https://github.com/Fpadt/acn.git
```

### Conda Environment

In order to be able to execute these jupyter notebooks one needs to setup the conda environment first.
This can be done with the following line of code, see [Creating an environment from an environment.yml file][conda_yml] for details. 

```
conda env create -f environment.yml
```

Note that after the environment is created it needs to be selected for the jupyter notebook by either

1. use the selector in the right upper corner of the jupyter notebook
1. use the **Command Palette**, see [vsc python interpreters][vsc_python_int] for details
    1. type \<CTRL\> + \<SHIFT\> + P 
    1. type ```>Python: Select Interpreter``` 
    1. select ```acn_py39``` from the list

In case the environment doesn't show you need to refresh the list, see [vsc additional notes][vsc_conda_env]

## Setup Secrets

As we use our own registrated API-key to extract data from ACN-Data using the Python-client one has to set up an ```.env``` file in the workspace with the API-key. 

Use the following code in the Terminal (WSL)

```
echo "export API_KEY=''" > .env
```

Documentation on API can be found here: [ACN - Data Client][acn_api]

## Run jupyter notebook

1. Open ACN-sim_L0x.ipynb 
1. execute the notebook

## Links

- [EV Research @ Caltech][def]  
- [ACNportal on GitHub][acnportal]  
- [ACM-sim Documentation][ACM-sim]  
- [ACNportal on PyPi][acn_portal_pypi]  

[def]:             https://ev.caltech.edu/index
[acnportal]:       https://github.com/zach401/acnportal
[ACM-sim]:         https://acnportal.readthedocs.io/en/latest/
[acn_portal_pypi]: https://pypi.org/project/acnportal/
[conda_yml]:       https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file
[vsc_python_int]:  https://code.visualstudio.com/docs/python/environments#_working-with-python-interpreters
[vsc_conda_env]:   https://code.visualstudio.com/docs/python/environments#_create-a-conda-environment-in-the-terminal
[acn_api]:         https://acnportal.readthedocs.io/en/latest/acndata/data_client.html


## Versioning

Note: this tool seems to use an old panda's version being:

[pandas python version][pandas-1.1.5]

[pandas-1.1.5]: https://pandas.pydata.org/pandas-docs/version/1.1.5/getting_started/install.html