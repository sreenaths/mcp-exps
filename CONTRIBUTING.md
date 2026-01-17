# Contributing to MCP Experiments

Thank you for your interest! This document outlines the guidelines and instructions for making contributions.

## Development Setup

1. Make sure you have Python 3.10+ installed
2. Install [uv](https://docs.astral.sh/uv/getting-started/installation/)
3. Fork the repository
4. Clone your fork
5. Install dependencies:

```bash
uv sync --frozen --all-extras --dev
```

6. Sets up the Git hook so it runs automatically on each git commit

```bash
uv run pre-commit install
```

## Development Workflow

1. In your fork, create a new branch from main or your chosen base branch.
2. Make your changes

3. Run type checking:

```bash
uv run pyright
```

4. Run linting:

```bash
uv run ruff check .
```

Fix and format

```bash
uv run ruff check . --fix
uv run ruff format .
```

5. Update README if you modified example code:
6. (Optional) Run pre-commit hooks on all files:

```bash
uv run pre-commit run --all-files
```

7. Submit a pull request to the same branch you branched from

### Code Style

- We use `ruff` for linting and formatting
- Follow PEP 8 style guidelines
- Add type hints to all functions
- Include docstrings for public APIs

## License

By contributing, you agree that your contributions will be licensed under [Apache License, Version 2.0](https://github.com/sreenaths/mcp-exps/blob/main/LICENSE)
