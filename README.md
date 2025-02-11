# automation_test
VID Credential Studio - Automation

Introduction: 
Automated testing project to validated the Api Endpoints whitin VIDIdentity, using Gherkin language and pytest-bdd framework

# Getting Started

IDEs Alternative to be selected:
Visual Studio Code:
https://code.visualstudio.com

Pycharm: 
https://www.jetbrains.com/pycharm/download/?section=windows

Install Pyhton:
For Windows operating system:https://www.python.org/downloads/ 
Find the version according to your system aschitecture, download and install, it´s important to check the field to add the Python Path in the system enviroment variables.
For GNU/Linux operating system: sudo apt-get install python3.12 
This version is according with the last version in the python site.

Install the following dependences: request: 
request: https://pypi.org/project/requests/pytest-env 
pytest-env: https://pypi.org/project/pytest-env/pytest-bdd
pytest-bdd: https://pypi.org/project/pytest-bdd/

For installation it is recommended to create a file with the name requirements.txt in the directory and execute the command:
     pip install -r requirements.txt
Build
     To build a test it is necessary to have the following directories and main files:

1. Create a test directory where all test directories and files will be hosted.
2. Create inside the "tests" directory a "features" subdirectory, in which all the files with extension .feature will be created, 
    which will contain the scenarios written in Gherkin language.
3. Create inside the test directory a subdirectory pages, in which will be created all the files with extension .py, 
    which will have, endpoints settings, global functions and necessary controls for the mapping of the scenarios.
4. Create within the "tests" directory, .py files linked to each .feature file, which will contain the logic that will allow 
    the execution of the events necessary for the tests.
5. Create inside the test directory, a file with the name pytest.ini, where the necessary environment variables with 
    the value to be configured in the pipeline will be saved.
6. Create inside the test directory, a file with the name pytest.dev.ini, where the necessary environment variables 
    will be saved with the value, this file allows to run the tests locally (this file must be ignored).
7. Create inside the test directory, a file with the name .gitignore, where the files that should not be uploaded to 
    the repository will be indicated.

Execution commands

     One of the following commands should be used:

    Run all tests:
        pytest -c pytest.dev.ini
     Run a specific test: 
       pytest -c .\pytest.dev.ini .\tests_00_file_name.py
    
Tools for formatting and analyzing code
    Install black to format the code:
        pip install black
    Install Pylint to find coding errors
        pip install pylint
        pylint rcfile generation
        pylint --generate-rcfile > pylintrc

Run to format and analyze code
     1. Run the following command before uploading changes to the repository:

    Linux: 
        black ./tests --diff
        Windows: 
        black ./tests --diff
    
    2. Execute the following command to find code improvements:
    Linux:
        pylint ./tests --output-format=colorized --rcfile=/.pylintrc
        Windows:
        pylint ./tests --output-format=colorized --rcfile=.pylintrc

Pytest must indicate a result of 100% to upload changes to the repository.