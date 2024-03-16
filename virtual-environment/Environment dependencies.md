```bash
(base) usr@project% pip install -r requirements.txt
```

```bash
(base) usr@project % pip freeze >> requirements.txt
```
# Module management systems (MMSs)
There are many different module management systems to choose from, but Anaconda is the most popular. 
However, it doesn’t always have the most up-to-date packages for data engineers, and ==pip==, the regular package manager for Python, ==doesn’t work well with Anaconda==.

## venv

[[venv]]
## pipenv
It’s a virtual environment and package management system that uses **Pipfile** and **Pipfile.lock**, similar to a **requirements.txt** file.

**$ pipenv install** or **$ pipenv uninstall** commands since activating the pipenv environment is designed to replace the need for the pip- tag in the command line.

**Pipfile.lock** is created to specify which version of the dependencies referenced in **Pipfile**
should be used to avoid automatic upgrades of packages that depend on each other. 
You can run the **$ pipenv lock** command to update the Pipfile.lock file with the currently used versions of all the dependencies within your virtual environment. However, pipenv takes care of updating the Pipfile and Pipfile.lock files with each package installation.