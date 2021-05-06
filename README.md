# Jupytext pre-commit hook
Hook for Jupytext with conda as a language.
Currently the main Jupytext-repo doesn't have pre-commit hooks defined, so 
this repo is called `mirror` only for consistency.

* For pre-commit: see https://github.com/pre-commit/pre-commit
* For Jupytext: see https://github.com/mwouts/jupytext

### Using Jupytext with pre-commit and conda:
Add this to your `.pre-commit-config.yaml`:

```yaml
- repo: https://github.com/Quantco/pre-commit-mirrors-jupytext
  rev: ''  # The git sha / tag you want to point to
  hooks:
    - id: jupytext-conda
      args:
        - --to=py:percent
```
`args` is optional and allows passing further parameters to `jupytext`.
By default only `--to=py:percent` is passed which converts all Jupyter notebooks to Python 
scripts using the [`percent` formatting](https://jupytext.readthedocs.io/en/latest/formats.html).
