---
type: guideline
trigger: When running tests in a Python project that uses uv for dependency management (indicated by pyproject.toml with uv.lock file)
trajectory: .evolve/trajectories/trajectory_2026-04-27T16-17-15.json
owner: vinodmut
source: vinodmut/test-evolve-guidelines
visibility: public
published_at: 2026-04-27T18:55:21Z
---

For uv-managed Python projects, use `uv run pytest` instead of `python3 -m pytest` to run tests

## Rationale

The uv tool manages the virtual environment and dependencies automatically. Using `uv run pytest` ensures tests run in the correct environment with all dependencies available, while direct python3 invocation may fail or use the wrong environment.
