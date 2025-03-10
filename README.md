# Jupyter notebooks
Collection of various Jupyter notebooks. This repo also defines my Jupyter
environment, notebook flow and requirements handling...

# Notebooks
- [Blunder buster](blunder-buster.ipynb)
- [Recommender](recommender.ipynb)

# Initialization
To initialize my jupyter environment on a new (Arch Linux) system, the
following needs to be done:

1. Install following system packages
    * jupyterlab-desktop-bin (from aur)
2. Create `notebooks` virtual environment and install requirements 
```
> mkvirtualenv notebooks
(notebooks) > pip install -r requirements.txt
```

# Flow
To create a new notebook:

1. Create new virtual environment and a new kernel for the notebook
```bash
> mkvirtualenv notebookXY 
(notebookXY) > pip install ipykernel
(notebookXY) > python -m ipykernel install --user --name=notebookXY --display-name "Python (notebookXY)"
```
2. Create requirements file `requirements/notebookXY.txt`
3. Install requirements
```bash
> workon notebookXY
(notebookXY) > pip install -r requirements/notebookXY.txt
```
4. Make sure you select the new kernel when creating new notebook
