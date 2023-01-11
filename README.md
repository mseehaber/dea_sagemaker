## Setting up a Custom Environment 

Similar to DE Africa's Sandbox, Amazon SageMaker Studio Lab uses a JupyterLab interface and includes the shared functionalities found in DE Africa's Sandbox. Including Functionalities such as GitHub intergration, preconfigured ML tools, frameworks and libraries. Amazon SageMaker Studio Lab is a free machine learning (ML) development environment that provides the compute, storage (up to 15GB), and security for users to learn and experiment with ML. 

The [deafrica_tools](https://docs.digitalearthafrica.org/en/latest/sandbox/notebooks/Tools/index.html) Python package contains modules with functions to load, analyse and output data from Digital Earth Africa. In the DE Africa Sandbox environment, this package is automatically installed. To utilise these functions external to DE Africa Sandbox we have installed this package as a dependcy in our environment. 

> Note: The Jupyter Notebook is an interactive web application which allows for the viewing, creating and documentation on code. Notebook applications include data transformation, visualisation, modelling and machine learning, all of which we are familar with from using DE Africa Sandbox.

## Setting up DE Africa's custom Environment in SageMaker Studio Lab

In this example we will use the environment.yml file to build a custom environment which include the necessary Python packages used to run DE Africa notebooks external to DE Africa Sandbox. Custom environments can be built in two ways in SageMaker Studio Lab. 

### Using Sagemaker Studio Lab UI 
Right click on the environment.yml file.

Select 'Build Conda Environment'. 

Confirm that you want to build the Conda environment by selecting 'Yes'. 

### Using the Terminal Console 
Open the Terminal window and use the following commands.

`conda env create -f environment.yml`

`conda activate`

Once the custom environment has been built, it will appear in the launcher. 

Upon opening one of DE Africa's notebooks, you will be prompted to select a kernel. From the dropdown select the 'dea-env' and press 'Select'. 

> Note: At the top right of your notebook the selected Kernel will be specified.

## Using the Custom Environment 

Once you have built the custom environment from the environment.yml file it will appear in the launcher. To run the Water Detection with Sentinel-1 notebook we need to specify our environment within the notebook. 

Upon opening the notebook, you will be prompted to ’Select Kernel’, from the dropdown chose the ‘dea-env’ kernel and press ‘Select’. 

You can also select the kernel from the upper right corner once the notebook is opened. 

> Note: This environment can be used to run other DE Africa notebooks however, existing notebooks will require changes to how the data is loaded in order for them to work in environments external to DE Africa Sandbox.

