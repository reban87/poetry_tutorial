# Poetry
Poetry is a tool for dependency management and packaging in Python. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you. Poetry offers a lockfile to ensure repeatable installs, and can build your project for distribution.


## Installation
To install Poetry (a dependency management and packaging tool for Python) on a Linux system, you can follow these steps:

### Step1: Install Poetry via the Official Script
Poetry provides an easy installation script that works across various Linux distributions.
- Open your terminal.
- Run the following command to install Poetry:
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

This command uses curl to download and run the Poetry installation script. It automatically installs the latest version of Poetry using python3.

- If you do not have ```curl``` installed, you can use ```wget```:
```bash 
wget -qO- https://install.python-poetry.org | python3 -
```

### Step2: Configure Your Environment
After installation, you need to add Poetry to your system's PATH to be able to use it from anywhere.

- For most Linux systems, Poetry installs itself into a directory in your home folder, typically ~/.local/bin. To ensure Poetry is available globally, add it to your PATH by running:
```bash
export PATH="$HOME/.local/bin:$PATH"
```

- To make this change permanent, add that line to your shell configuration file (e.g., ~/.bashrc for Bash or ~/.zshrc for Zsh). After adding the line, reload the shell:
```bash
source ~/.bashrc  # or source ~/.zshrc
```

### Step3: Verify Installation
```bash
poetry --version
```

## Create a virtual environment 

### 1. Using Python's Built-in venv Module
1. Open your terminal.
2. Navigate to your project directory (if you haven't already):

```bash
cd /path/to/your/project
```
3. Create the virtual environment:
```bash
python3 -m venv venv
```
This command creates a new virtual environment named venv (you can choose a different name) in your project directory.

4. Activate the virtual environment:
```bash
source venv/bin/activate
```
Confirm the virtual environment is active by checking your prompt. It should show the name of the virtual environment, like (venv).

5. Deactivate the virtual environment when you're done working:
```bash
deactivate
```

### 2. Using Poetry 

If you're using Poetry to manage dependencies and create a virtual environment, it simplifies the process for you.
1. Navigate to your project directory (if you haven't already):
```bash
cd /path/to/your/project
```

2. Create a new Poetry project (if you haven't already):
```bash
poetry new my-project
cd my-project
```
3. Install the dependencies and create the virtual environment:
```bash
poetry install
```
Poetry will automatically create a virtual environment and install dependencies listed in the pyproject.toml file.

4. Activate the virtual environment:
```bash
poetry shell
```
This activates the virtual environment Poetry created for you, and the prompt will change to indicate that you are inside the virtual environment.

5. Deactivate the virtual environment when you're done working:
```bash
exit
```

### 3. Using ```virtualenv``` 
If you prefer using the virtualenv tool (an older but widely-used option):
1. Install virtualenv (if it's not already installed):
```bash
pip install virtualenv
```
2. Navigate to your project directory:
```bash
cd /path/to/your/project
```
3. Create the virtual environment:
```bash
virtualenv venv
```
4. Activate the virtual environment:
```bash
source venv/bin/activate
```
5. Deactivate the virtual environment when you're done working:
```bash
deactivate
```
 
Conclusion:
- For simple virtual environments: Use the venv module (python3 -m venv).
- For Python project management with dependencies: Use Poetry (poetry install and poetry shell).
- For an alternative to venv: Use virtualenv (virtualenv venv).