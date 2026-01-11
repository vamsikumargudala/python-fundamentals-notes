# Python Project Setup Guide

A practical guide to setting up Python projects using UV and VS Code.

---

## 1. Initialize Git Repository

```bash
git init
```

This creates a `.git/` folder to track your project history.

### Create .gitignore

A `.gitignore` file tells Git which files to ignore. Common entries for Python projects:

```gitignore
# Virtual environment
.venv/

# Python cache
__pycache__/
*.pyc

# Jupyter checkpoints
.ipynb_checkpoints/

# IDE settings
.vscode/
.idea/

# OS files
.DS_Store
Thumbs.db

# UV lock file (optional - commit if you want reproducible builds)
uv.lock
```

---

## 2. UV - Python Package Manager

UV is a fast Python package manager written in Rust. It replaces pip and handles virtual environments.

### Install UV

```bash
pip install uv
```

### Create Virtual Environment

```bash
uv venv
```

This creates a `.venv/` folder with an isolated Python installation.

### Activate Environment

**Git Bash:**
```bash
source .venv/Scripts/activate
```

**CMD / PowerShell:**
```cmd
.venv\Scripts\activate
```

You'll see `(.venv)` in your terminal prompt when active.

### Deactivate

```bash
deactivate
```

---

## 3. pyproject.toml

This is the modern Python project configuration file. It replaces `setup.py` and `requirements.txt`.

### Basic Structure

```toml
[project]
name = "my-project"
version = "0.1.0"
description = "Project description"
requires-python = ">=3.8"

dependencies = [
    "pandas>=2.0",
    "numpy>=1.24",
]

[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"
```

### With Dev Dependencies

```toml
[project]
name = "my-project"
version = "0.1.0"
requires-python = ">=3.8"

dependencies = [
    "pandas>=2.0",
    "numpy>=1.24",
]

[project.optional-dependencies]
dev = [
    "pytest>=7.0",
    "black>=23.0",
    "flake8>=6.0",
]

[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"
```

---

## 4. UV Commands

### Install Dependencies

```bash
# Install from pyproject.toml
uv sync

# Install including dev dependencies
uv sync --all-extras
```

### Add Packages

```bash
# Add a package (updates pyproject.toml automatically)
uv add pandas

# Add with version constraint
uv add "numpy>=1.24"

# Add multiple packages
uv add pandas numpy matplotlib

# Add dev dependency
uv add --dev pytest black
```

### Remove Packages

```bash
uv remove pandas
```

### Update Packages

```bash
# Update all
uv sync --upgrade

# Update specific package
uv add pandas --upgrade
```

### List Installed Packages

```bash
uv pip list
```

### Lock Dependencies

UV automatically creates `uv.lock` when you run `uv sync`. This locks exact versions for reproducible installs.

```bash
# Recreate lock file
uv lock

# Install from lock file (CI/CD)
uv sync --frozen
```

---

## 5. Jupyter Notebooks in VS Code

### Install Required Packages

```bash
uv add jupyter notebook ipykernel
```

### VS Code Extensions

Install these extensions:
- Python (ms-python.python)
- Jupyter (ms-toolsai.jupyter)

### Select Python Interpreter

1. Press `Ctrl+Shift+P`
2. Type "Python: Select Interpreter"
3. Choose `.venv\Scripts\python.exe`

### Register Jupyter Kernel (Optional)

If the notebook doesn't detect your environment:

```bash
python -m ipykernel install --user --name=my-project --display-name="My Project"
```

### Using Notebooks

1. Open any `.ipynb` file in VS Code
2. Click "Select Kernel" in the top right
3. Choose your `.venv` Python interpreter
4. Run cells with `Shift+Enter`

---

## 6. Project Structure Example

```
my-project/
├── .git/
├── .gitignore
├── .venv/
├── pyproject.toml
├── uv.lock
├── src/
│   └── my_module.py
├── notebooks/
│   └── analysis.ipynb
└── tests/
    └── test_my_module.py
```

---

## 7. Common Workflows

### Starting a New Project

```bash
mkdir my-project
cd my-project
git init
uv venv
source .venv/Scripts/activate
uv init  # creates pyproject.toml
uv add pandas numpy matplotlib jupyter
```

### Cloning an Existing Project

```bash
git clone <repo-url>
cd my-project
uv venv
source .venv/Scripts/activate
uv sync
```

### Daily Development

```bash
# Activate environment
source .venv/Scripts/activate

# Add new package when needed
uv add requests

# Run your code
python my_script.py

# Deactivate when done
deactivate
```

---

## 8. Troubleshooting

### "Python not found"

Check Python is installed and in PATH:
```bash
python --version
```

Or specify Python path:
```bash
uv venv --python /path/to/python
```

### Kernel not showing in VS Code

Re-register the kernel:
```bash
python -m ipykernel install --user --name=my-project
```

Then restart VS Code.

### Permission errors on Windows

Run terminal as Administrator, or use:
```bash
uv sync --user
```

---

## Quick Reference

| Task | Command |
|------|---------|
| Create venv | `uv venv` |
| Activate | `source .venv/Scripts/activate` |
| Install deps | `uv sync` |
| Add package | `uv add <package>` |
| Add dev package | `uv add --dev <package>` |
| Remove package | `uv remove <package>` |
| Update all | `uv sync --upgrade` |
| List packages | `uv pip list` |
