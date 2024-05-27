# Clustering Experiment
Experiment setup to create a knowledge graph from *Reddit* posts. For details, please refer to the notebooks, which implement the experiment.

# How to run
## Requirements
* Running *Ollama* server: https://ollama.com/ with `llama3` model. The used model might change if this experiment is carried on.
* Python3

## Install and run
The experiment includes a `Makefile`.

`make run` starts up a *Jupyter notebook*  server. Additionally, a browser window with the Jupyter UI should open.

There are more fine-grained make targets available: `setup`, `install`, `clean`.

The notebooks should be run in order, because they locally store intermediate results, which are computationally expensive or which require calling external APIs. Please refer to the notebooks for details.

In general, run:
1. download-reddit-data.ipynb
2. create-embeddings.ipynb
3. cluster.ipynb
