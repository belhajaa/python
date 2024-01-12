## Pip 

Package installer for python : it's a command line tool that allows developpers to install, upgrade and manage Python Package and dependencies.

```bash
pip install package_name
pip install package_name==version_number
pip uninstall package_name
pip list
pip freeze > requirements.txt
pip install -r requirements.txt
```
## virtual envirement
follow this video on Youtube : https://www.youtube.com/watch?v=KxvKCSwlUv8

Create a venv called venvName in the project folder
```bash
python3 -m venv venvName
```
Then, we activate the virtual envirement via the command source

```bash
source venv/bin/activate
``
the (venvName) tells us that the venv go activated
```bash
(venvName) ahmed@ahmed-HP:~/Dev/Python/SingleFeatureProjects/setup-venv$ 
```

Now, if we install a package via pip it will be installed in the activated virtual enviremnt.

We follow the list of dependencies of python project via requirements.txt file.
 and we use pip freeze and pip install -r to setup the required packages. 


