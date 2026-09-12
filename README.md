# Authipy

<div align="center">

[![PyPI Version](https://img.shields.io/pypi/v/Authipy.svg)](https://pypi.org/project/Authipy)
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://python.org)
[![License](https://img.shields.io/github/license/TanmoyTheBoT/authipy.svg)](LICENSE)
[![Downloads](https://img.shields.io/github/downloads/TanmoyTheBoT/authipy/total.svg)](https://github.com/TanmoyTheBoT/authipy/releases)

A secure, offline Two-Factor Authentication (2FA) desktop application.

[Features](#features) • [Installation](#installation) • [Usage](#usage) • [Contributing](#contributing)

<img src="https://raw.githubusercontent.com/TanmoyTheBoT/Authipy/master/docs/images/screenshot.png" alt="Authipy Screenshot" width="400">

</div>

## Features

- 🔒 Secure TOTP code generation
- 💾 Local-only storage
- 📱 QR code import/export
- 🗑️ Recycle bin feature
- 📋 One-click copying
- ⚡ Modern Qt interface

## Installation

### Method 1: Windows Executable (Recommended)
1. Download the latest `Authipy.exe` from [Releases](https://github.com/TanmoyTheBoT/authipy/releases)
2. Run directly - No installation required

### Method 2: PyPI Package
```bash
pip install authipy
authipy  # to run
```

### Method 3: Build from Source with uv

1. Clone the repository:
```bash
git clone https://github.com/TanmoyTheBoT/authipy.git
cd authipy
```

2. Install uv if needed:
```bash
pip install uv
```

3. Sync the project environment and dev dependencies:
```bash
uv sync --group dev
```

4. Run the application:
```bash
uv run authipy
```

5. Build the Python package (optional):
```bash
uv build
```

6. Build a single-file executable (optional):
```bash
# Install PyInstaller
uv pip install pyinstaller

# Build single-file executable
uv run python -m PyInstaller --noconsole --onefile --icon=docs/images/test.jpg --name Authipy --distpath exe-dist src/authipy/main.py
```

The executable will be created in the `exe-dist` directory.

## Usage

### Add New Account
1. Click "Add Account"
2. Enter:
   - Service name (required)
   - Secret key (required)
   - Issuer name (optional)

### Generate Codes
- Select account from list
- Code displays automatically
- Click code to copy

### Manage Accounts
- Right-click for options
- Use recycle bin
- Import/Export accounts

### Data Location
- Windows: `%USERPROFILE%\.config\authipy`
- Offline storage only

## Contributing

1. Fork the repository
2. Install the project and dev dependencies:
```bash
uv sync --group dev
```
3. Make changes
4. Run tests:
```bash
uv run pytest
uv run pytest --cov=src --cov-report=html  # coverage report
```
5. Submit Pull Request

## Support

- [Report Issues](https://github.com/TanmoyTheBoT/authipy/issues)
- [GitHub Repository](https://github.com/TanmoyTheBoT/authipy)

## License

[MIT License](LICENSE)

---
<div align="center">
<sub>Built with ❤️ by <a href="https://github.com/TanmoyTheBoT">TanmoyTheBoT</a></sub>
</div>
