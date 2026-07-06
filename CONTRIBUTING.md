# Contributing

Thanks for helping improve DarvasTrader.

## How to contribute

1. Fork the repository and create a feature branch.
2. Keep changes focused and clearly described.
3. Update documentation when behavior or setup changes.
4. Avoid committing generated scan artifacts, API keys, or local environment files.

## Development setup

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r scanner/requirements.txt
```

## Suggested checks

Before opening a pull request, verify that your changes still run cleanly:

```bash
python -m compileall agents portfolio scanner
```

## Pull request notes

Please include:
- a short summary of the change
- any relevant context or screenshots
- the reason the change is useful

Thank you for contributing.
