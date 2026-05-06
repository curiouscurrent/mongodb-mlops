# mongodb-mlops

1. Create project template by executing template.py file
2. Write the code on setup.py and pyproject.toml to import local packages. 
3. Create a virtual env, activate it and install the requirements from requirements.txt 
i) Create a virtual environment named 'vehicle'
```
python -m venv vehicle
```
ii) Activate the environment (windows - cmd)
```
vehicle\Scripts\activate.bat
```
iii) To deactive the environment 
```
deactivate
```
iii) Add required modules to requirements.txt, by doing
```
pip install -r requirements.txt
```
4. Do a "pip list" on terminal to make sure you have local packages installed. 
5. Include -e . in requirements.txt to install all the local packages from src folder in your "vehicle" environment.
