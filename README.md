`punwrap` provides only Python bindings for
[`runwrap`](https://github.com/veikman/runwrap), a Rust library for wrapping
and unwrapping paragraphs of Markdown.

For an example of higher-level utilities built on `punwrap`, see
[`yamlwrap`](https://github.com/veikman/yamlwrap).

## Maintenance

Binary builds are automated through GitHub. To add support for a new version of
Python, or remove support, edit:

| File | Relevance |
| ---- | --------- |
| `.github/workflows/build.yml` | The central build environment and its outputs. |
| `pyproject.toml` | Trove classifiers and requirements for the Python project, which will appear on PyPI. |
| `tasks.py` | `PYTHON_INTERPRETER_VERSIONS` governs local builds only. |

For this and other release-relevant changes, add notes to `CHANGELOG.md`.

| File | Action |
| ---- | ------ |
| `CHANGELOG.md` | Finalize release notes. |
| `README.md` | Update copyright statement. |
| `Cargo.toml` | Update version ID. |

Commit it all, push to GitHub, and observe the build actions there. For a
release, apply a Git tag, push the tag, observe the new build, and observe the
release appearing on PyPI.

## License

Copyright 2021–2026 Viktor Eikman

`punwrap` is licensed as detailed in the accompanying file LICENSE.
