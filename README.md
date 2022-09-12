# PRIOR

[![DOI](https://zenodo.org/badge/497726192.svg)](https://zenodo.org/badge/latestdoi/497726192)

🐍 A Python package for distributing resources from AI2's PRIOR team

## Installation

Install the `prior` package with pip:

```bash
pip install prior
```

## Datasets

- ProcTHOR-10k [[GitHub]](https://github.com/allenai/procthor-10k)

```python
import prior
prior.load_dataset("procthor-10k")
```

- Object Nav Evaluation [[GitHub]](https://github.com/allenai/object-nav-eval)

```python
import prior
prior.load_dataset("object-nav-eval")
```

## Models

- ProcTHOR Models [[GitHub]](https://github.com/allenai/procthor-models)

```python
import prior
prior.load_model(project="procthor-models", model="object-nav-pretraining")
```

## Example Usage

To use a public Python dataset, simply run:

```python
import prior
dataset = prior.load_dataset("test-dataset", entity="mattdeitke", revision="main")
```

Here, `revision` can be either a tag, branch, or commit hash.

## Private Datasets

If you want to use a private dataset, make sure you're either:

1. Already logged into GitHub from the command line, and able to pull a private repo.
2. Set the GITHUB_TOKEN environment variable to a GitHub authentication token with read access to private repositories (e.g., `export GITHUB_TOKEN=<token>`). You can generate a GitHub authentication token [here](https://github.com/settings/tokens).
3. Set the `gh_auth_token` global variable in the `prior` package with:

```python
import prior
prior.gh_auth_token = "<token>"
```

## Citation

To cite the PRIOR package, please cite use:

```bibtex
@software{prior,
  author={Matt Deitke and Aniruddha Kembhavi and Luca Weihs},
  doi={10.5281/zenodo.7072830},
  title={{PRIOR: A Python Package for Seamless Data Distribution in AI Workflows}},
  url={https://github.com/github/allenai/prior},
  year={2022}
}
```
