# Python Virtual Environment Setup

This guide explains how to create and use a Python virtual environment.

## Why Use a Virtual Environment?

A virtual environment keeps project dependencies isolated from other Python projects on your system.

Benefits:

- Separate packages for each project
- Avoid version conflicts
- Easier project management
- Professional development practice

---

## 1. Check Python Installation

```bash
python --version
```



```bash
python3 --version


## Common Commands

| Task | Command |
|--------|---------|
| Create venv | `python -m venv venv` |
| Activate (Windows) | `venv\Scripts\activate` |
| Activate (PowerShell) | `.\venv\Scripts\Activate.ps1` |
| Activate (Linux/macOS) | `source venv/bin/activate` |
| Install package | `pip install package_name` |
| Save dependencies | `pip freeze > requirements.txt` |
| Install requirements | `pip install -r requirements.txt` |
| Deactivate | `deactivate` |
