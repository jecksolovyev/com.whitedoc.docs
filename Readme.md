# WhiteDoc ReadTheDocs documentation manual 

## Installation of the required sources

### Windows

1. Install the latest version of Python from https://www.python.org/downloads/
2. Update PIP to the latest version: in powershell run `python -m pip install --upgrade pip`
3. Install all dependencies from the requirements file: in powershell run `pip install -r requirements.txt`
4. Periodically check if any packages should be updated: in powershell run `pip list --outdated`
5. If any packages show that newer version is available: in powershell run `pip freeze | %{$_.split('==')[0]} | %{pip install --upgrade $_}`

### Linux, MacOS

1. Update all packages: `sudo apt update && sudo apt upgrade -y`
2. Install PIP: `sudo apt install python3-pip`
3. Install all dependencies from the requirements file: `sudo pip install -r requirements.txt`
4. Periodically run first step again to keep all packages up to date

You will have everything ready after this. To build a local copy of documentation with your latest updates run next command from /docs folder: `.\make.bat html`

## Documentation creation rules

When we want to create new documentation page we have to follow the heirarchy functionality in documentation. 

So, if we want to create documentation related to user authorization on platform we have to create file with 
extension .rst in docs/source/pages/howToWorkWithPlatform/authorization/login folder.

After file creation we have to link it with head file of the folder (according to example it would be 
docs/source/pages/howToWorkWithPlatform/authorization/autorization.rst). 

To create link head file with child files we have to add to head file link to child file. It could be done two ways:

1. Link it directly within ref functionality

```
:ref:`log in <login>`
```

2. Add link to file within toctree functionality 

```
.. toctree::

pages/howToWorkWithPlatform/howToWorkWithPlatform.rst
pages/api/api.rst
pages/errorCodes/errorCodes.rst
pages/configuration/configuration.rst
pages/clients/clients.rst
```

As soon as files linked we could start fill in content of the documentation page. To fill documentation we have to use 
markdown which presented in sphinx documentation https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html.