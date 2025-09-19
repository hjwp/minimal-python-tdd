# Minimal Python TDD project template

A minimal 2-file setup for doing TDD in Python, eg for code katas.

* Tests live in `tests.py`
* Code lives in `kata.py`  (obviously feel free to move/rename as you wish)
* Includes 1 placeholder test & function


## Dependencies

* pytest
* (optionally) mypy
* (optionally) [watchexec](https://github.com/watchexec/watchexec), a file-watching command re-runner.


## Installation instructions

Create a virtualenv and install pytest.  Eg:


```sh
uv venv
uv pip install .
```

([uv is great](https://www.youtube.com/watch?v=8UuW8o4bHbw) so if you haven't tried it out yet,
 could today be a good excuse?  [uv install instructions](https://docs.astral.sh/uv/getting-started/installation/))


## Test run

```sh
pytest 
# or if you're all-in on uv:
uv run pytest
````

## Auto-run 

```sh
# run tests on every file change
watchexec pytest
# or
watchexec uv run pytest

# (in a separate terminal)
# run mypy on every file change. notice the "."
watchexec mypy .
# or
watchexec uv run mypy .
```
