# Python Virtual Environment Setup

This guide explains how to create and use a Python virtual environment.

## Why Use a Virtual Environment?

A virtual environment keeps project dependencies isolated from other Python projects on your system.

Benefits:

- Separate packages for each project
- Avoid version conflicts
- Easier project management
- Professional development practice



## 1. Check Python Installation


python --version
python3 --version

## Common Commands

| Action | Command |
|----------|----------|
| Create Virtual Environment | `python -m venv venv` |
| Activate (Windows CMD) | `venv\Scripts\activate` |
| Activate (Windows PowerShell) | `.\venv\Scripts\Activate.ps1` |
| Activate (Linux/macOS) | `source venv/bin/activate` |
| Install Package | `pip install package_name` |
| View Installed Packages | `pip list` |
| Save Dependencies | `pip freeze > requirements.txt` |
| Install Dependencies | `pip install -r requirements.txt` |
| Deactivate Environment | `deactivate` |
| Delete Virtual Environment | Delete the `venv` folder |

### Example Workflow

# Create virtual environment
python -m venv venv

# Activate virtual environment
venv\Scripts\activate

# Install packages
pip install requests

# Save dependencies
pip freeze > requirements.txt

# Exit virtual environment
deactivate
```
