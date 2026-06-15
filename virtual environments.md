learning record(Mainly records the learning process of becoming a black-hat programmer in Python + AI without prior knowledge. It covers the entire process of developing practical Python projects, including core Python syntax, AI applications, data analysis, and web applications)



First, we need to configure the environment. Since the BlackHorse project requires downloading Python version 3.13.9, and there is already Python version 3.11 installed on my computer, version management is necessary. The method I chose was to use a virtual environment, creating a virtual environment for each project.

Method 1: conda

1.conda info --envs(View current environment)

2.conda create -n py3.13 python=3.\_\_(where 3.13 is the desired Python version, and the rest is the name)

3.You can once again check the current environment to see if the creation was successful.

4.conda activate (activates the environment by using the name of the virtual environment you just set up.)

5.python -c "import sys; "print(sys.executable)" (To view the path of the current environment)

6.conda deactivate(exit the current virtual environment)

Method 2:venv

1.python -m venv venv(Create a virtual environment)

2..\\venv\\Scripts\\Activate.ps1(Activate the virtual environment of the terminal)

3.If there is a problem with PowerShell permissions: Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope

4.Batch Installation List: pip install -r ./requirements.txt

5.Each time the debugging is successful, if there is a library change, export requirements.txt: pip list --format=freeze > requirements.txt

***------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------***

***virtual environments：***

The way to directly call Python in the Windows system is to add the directory where python.exe is located in the system variables.

When calling Python in a virtual environment, it is configured with the Python path in the virtual environment's configuration.

When installing Conda (Anaconda, Miniconda are the same), it will automatically bring a bound and paired version of the Python environment (such as: python3.11). After installation, there seems to be a pop-up window or option asking whether to use base as the default Python environment for the system (if so, remove the Python path in the system variables. Open PowerShell and activate Base by default. If deactivate base, directly calling the python command in the system will not find python).

It is possible that the previous system's inability to find python was caused by this option; another possibility is that you later downloaded a separate Python installer and when installing the new one, it would first clean up the old one, and Python does not support multiple versions to coexist directly.

Components of the Python environment (that you come into contact with):

Part P1 - Python interpreter, compiler

Part P2 - Built-in libraries

Part P3 - Third-party package component libraries



When creating a virtual environment using conda, there are several key steps:

1\. Create the P1 section

2\. Copy the P2 section

3\. Copy or download and compile the P3 section

The differences between specifying the Python version and not specifying it:

1\. If the Python version is not specified, the default bound Python version will be used, which is usually the same as the base version. Just copy P1P2P3 and then compile the environment.

2\. If the Python version is specified, check if there is a corresponding version of P1P2P3 in the local conda environment management cache. If it exists with the specified version, directly copy and compile. If not, download them in sequence and then compile.

***summary：***

Therefore, when deciding whether the same virtual environment can be used for different projects, several aspects need to be considered. Firstly, do the two projects have any connection? Projects that are related should be placed in the same environment, unless they are truly incompatible. In addition, if the projects are not related, it should be considered whether the versions of the used Python are the same. Both P1 and P2 are strongly related to the Python version. The library of P3, in addition to relying on P1 and P2, may also have version dependencies directly among itself.

The pip install xxxx command installs the package library of P3 part. After considering P1 and P2, it is also necessary to consider whether P3 is compatible with each package and whether the packages of the new project will have an impact on the old project, or whether the packages will have an impact on the project after upgrading. There is another situation where the new project is a simple test version and only conducts simple tests. The packages used by P3 are only basic packages, so it is also possible to consider using the same virtual environment. In summary, whether two projects can use the same virtual environment should be considered, taking into account the degree of association, compatibility, and difficulty of the new project.

\------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

