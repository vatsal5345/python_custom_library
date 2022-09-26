# python_custom_library

This folder structure contains the fuctionality to create and import a custom-made library that can be used anywhere in project.


1) Create a separate folder for the library and cd to the new folder path.
2) Create a venv in that folder.
3) install following in the venv
	- pip install wheel
	- pip install setuptools
	- pip install twine
4) Create an empty file called setup.py & README.md in the main folder outside venv.
5) Create a folder called mypythonlib, or whatever you want your Python library to be called when you 	pip install it. (The name should be unique on pip if you want to publish it later.)
6) Create an empty file inside mypythonlib that is called "__init__.py". Put minimal code inside it 	as init file is called first when lib is imported. but leave it empty if nothing to be put inside.
	Also, in the same folder, create a file called myfunctions.py.
7) Create a folder tests in your root/main folder. Inside, create an empty __init__.py file and an 	empty test_myfunctions.py.
8) Put functionality.py(any name to give) file in folder created in Step-5.
9) Install 
	- pip install pytest==4.4.1
	- pip install pytest-runner==4.4
to run tests on your code.
10) Put test code in a file in tests folder.
11) Finally write code in setup.py to run your library.
12) Run setup to test codes by "python setup.py pytest"
13) To build the lib, use 'python setup.py bdist_wheel'
14) Now the zip file for the compiled lib is created in the dist folder.

Install the zip file(package/lib) with pip command and its ready to be imported in project.

(CAUTION : Just ot be sure, if lib does not show when trying to import, try installing it in local too.)

source : https://medium.com/analytics-vidhya/how-to-create-a-python-library-7d5aea80cc3f
