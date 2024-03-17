# some-notebooks


## Creating virtual environment
- `sudo apt install python3.10-venv`
- `python3 -m venv ./venv/some_notebooks_env`
- `source ./venv/some_notebooks_env/bin/activate`


## Installing base libs
- `pip install -r requirements.txt`


## Generate jupyter notebook config
- `jupyter notebook --generate-config` (writes by default to ~/.jupyter/jupyter_notebook_config.py)
- append to the generated config:
```
c.NotebookApp.contents_manager_class="jupytext.TextFileContentsManager"
c.ContentsManager.default_jupytext_formats = ".ipynb,.Rmd"
```


## Add current venv as notebook kernel (ipykernel)
- `python -m ipykernel install --user --name some_notebooks_env`


## Start notebook server
- `jupyter notebook`
- Select the kernel matching the above specified name (in this case `some_notebooks_env`)