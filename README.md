#  Paul 

---
## Authors
* Vojtěch Kaše


## License
CC-BY-SA 4.0, see attached License.md

---
# Getting started

* download or clone the repository
* go to Terminal and move to that directory
* run the following bash commands (modify the `$VENVNAME` variable value as you wish):
```
# check which python will be by default used as a source for your virtualenv
# (otherwise specify manually when defining the INTERPRETER variable)
which python3

# check that your pip is python 3 pip:
pip --version
# install virtualenv package
pip install virtualenv

INTERPRETER=$"which python3" # or any other interpreter, e.g. $HOME/.local/lib/python-3.9.7/bin/python3
virtualenv paul_venv --python=$INTERPRETER

# install anything in requirements.txt:
paul_venv/bin/python -m pip install -r requirements.txt 

# create jupyter kernel based on the environment:
paul_venv/bin/python -m ipykernel install --user --name=paul_venv

# create folder for large files:
mkdir data/large_files

# check that it is included in your `.gitignore` file
echo "/$VENVNAME/
/data/large_files/" > .gitignore

```

* subsequently, in all jupyter notebooks, always check that you are connected to the correct kernel 
* (alternatively, if you do not wish to use virtual environment, make sure that you have installed all required python packages within the `requirements.txt` file: `pip install -r requiremnts.txt`)

---
## Scripts 
The scripts are in the `scripts` subfolder and their numbers and titles should be self-explanatory. Usually, they have the form of Jupyter notebooks.
