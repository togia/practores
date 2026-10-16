# practores
Experiments with agentic systems

## Setup

Requires [uv](https://docs.astral.sh/uv/).

```bash
uv sync
```

This creates `.venv` with Python 3.13 and installs `crewai` and `crewai-tools`.

## Usage

Run a script inside the project environment:

```bash
uv run python your_script.py
```

Check the install:

```bash
uv run python -c "import crewai, crewai_tools; print(crewai.__version__)"
```

## Notes

- Python is pinned to 3.13 because crewai does not support 3.14 yet.
- `crewai` and `crewai-tools` are pinned to 1.6.1, the newest release that
  installs on Intel (x86_64) macOS. Newer releases depend on `lancedb`
  versions that ship no Intel Mac wheels. On Apple Silicon or Linux, you can
  drop the pins and the `[tool.uv]` section in `pyproject.toml` to get the
  latest versions.
