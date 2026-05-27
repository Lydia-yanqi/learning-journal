# learning-journal
learning record(Mainly records the learning process of becoming a black-hat programmer in Python + AI without prior knowledge. It covers the entire process of developing practical Python projects, including core Python syntax, AI applications, data analysis, and web applications)
First, we need to configure the environment. Since the BlackHorse project requires downloading Python version 3.13.9, and there is already Python version 3.11 installed on my computer, version management is necessary. The method I chose was to use a virtual environment, creating a virtual environment for each project.
Method 1: conda
1.conda info --envs(View current environment)
2.conda create -n py3.13 python=3.__(where 3.13 is the desired Python version, and the rest is the name)
3.You can once again check the current environment to see if the creation was successful.
4.conda activate (activates the environment by using the name of the virtual environment you just set up.)
5.python -c "import sys; "print(sys.executable)" (To view the path of the current environment)
6.conda deactivate(exit the current virtual environment)
Method 2:venv
1.python -m venv venv(Create a virtual environment)
2..\venv\Scripts\Activate.ps1(Activate the virtual environment of the terminal)
3.If there is a problem with PowerShell permissions: Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope
4.Batch Installation List: pip install -r ./requirements.txt
5.Each time the debugging is successful, if there is a library change, export requirements.txt: pip list --format=freeze > requirements.txt
