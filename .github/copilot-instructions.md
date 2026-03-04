# Copilot Instructions for generator-domiciliation-docs

## Project Overview

This is a Python project for generating domiciliation (residence/address) documentation. Currently in early development stages (v0.1.0), it uses:
- **Python 3.13** (specified in `.python-version` and `pyproject.toml`)
- **uv** package manager (indicated by `uv.lock`)
- **No external dependencies** currently

## Development Environment

### Setup
1. Ensure Python 3.13 is installed
2. Run with uv: `uv run python main.py`
3. Or use venv: `.venv/Scripts/Activate.ps1` (PowerShell on Windows)

### Package Management
- Dependencies are declared in `pyproject.toml` under `[project]` and `[project.optional-dependencies]`
- Lock file: `uv.lock` (keep updated when adding dependencies)
- Add packages: `uv add package-name` (preferred over pip)

## Architecture & Code Patterns

### Entry Point
- `main.py` is the application entry point
- Currently contains minimal boilerplate; expand here for orchestration logic

### Project Structure Patterns
- Keep the codebase flat initially (single `main.py`)
- When adding modules, follow Python conventions: create subdirectories as packages with `__init__.py`
- For document generation logic, consider creating `generators/` or `templates/` packages

## Important Notes

- **No existing conventions**: This is a fresh project with no established patterns yet
- **Minimal dependencies**: Keep the dependency footprint small—evaluate all additions carefully
- **Git workflow**: Current branch is `master` with initial commit only

## When Implementing Features

1. **Update `pyproject.toml`** when adding dependencies (description field is currently generic)
2. **Maintain Python 3.13 compatibility** (don't use features from newer versions)
3. **Use uv for consistency** if adding development tools
4. **Document CLI arguments** and configuration in README.md as the project grows
5. **Keep main.py** as the entry orchestrator; move logic into modules

## Future Development Priorities

- Define the document generation domain model (what's a "domiciliation document"?)
- Establish templates or schema for output documents
- Add configuration management (file-based or CLI args)
