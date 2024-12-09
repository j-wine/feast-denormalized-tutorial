# feast-denormalized-tutorial
Feast + Denormalized

This repository contains an example application of using [Denormalized](https://www.denormalized.io/) to process features in real-time and sink them to an online feast store.


## Getting started

- `uv venv --python 3.12 && .venv/bin/activate`
- `uv sync --dev`
- `uv pip install -e .`


- Start kafka in docker `docker run -p 9092:9092 --name kafka apache/kafka`
- create the feature store: `python src/feature_repo/` 
- Start emitting events: `python src/session_generator/`
- Start the pipelines: `python src/pipelines/`

The features can be viewed in realtime using the `print_features.ipynb` notebook
`jupyter-lab`
