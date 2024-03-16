`venv` is a Python module that provides support for creating lightweight, isolated Python environments. Here are the basic steps for managing virtual environments using `venv`:

### 1. Creating a Virtual Environment:
```bash
python3 -m venv venv
```
This will create a new directory named `venv` that contains the virtual environment.

### 2. Activating the Virtual Environment:
```bash
source venv/bin/activate
```
After activation, your command prompt or terminal should change to indicate the name of the virtual environment.

### 3. Installing Packages:
Once the virtual environment is activated, you can install packages using `pip`. For example:
```bash
pip install package_name
```

### 4. Deactivating the Virtual Environment:
To deactivate the virtual environment and return to the global Python environment, simply run:
```bash
deactivate
```

### 5. Freezing Installed Packages:
To freeze the installed packages along with their versions into a `requirements.txt` file:
```bash
pip freeze > requirements.txt
```

### 6. Installing Packages from `requirements.txt`:
To install packages from a `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### 7. Deleting the Virtual Environment:
Simply delete the `venv` directory to remove the virtual environment.

### Tips:
- Always activate the virtual environment before working on a project to isolate dependencies.
- Use `requirements.txt` to document and reproduce the environment on another machine.
- Make sure to add `venv/` to your project's `.gitignore` to avoid versioning the virtual environment.

Managing virtual environments with `venv` provides a clean and isolated environment for your Python projects, helping to avoid conflicts between different projects' dependencies.