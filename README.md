# jupytext pre-commit hook

pre-commit hook of jupytext with conda as a `language` / package manager.

For pre-commit: see [here](https://github.com/pre-commit/pre-commit)

For jupytext: see [here](https://github.com/mwouts/jupytext)

## Using jupytext with pre-commit and conda:

Add this to your `.pre-commit-config.yaml`

```yaml
 - repo: https://github.com/quantco/pre-commit-mirrors-jupytext
   rev: ''  # Use the sha / tag you want to point at
   hooks:
     - id: jupytext-conda
```
