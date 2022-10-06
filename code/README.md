All Jupyter notebooks can be found in this directory.

# Requirements

We tested these artifacts with `Python 3.10` with the following additional requirements:

```
numpy
pandas
matplotlib
seaborn
zstandard
jupyterlab
```

You can install them via pip with `pip install -r requirements.txt`. We recommend installing the dependencies in a virtual environment:

```bash
$ python3 -m venv envs
$ source envs/bin/activate
$ pip install -r requirements.txt
$ # Reproduce the results: see 'How to Reproduce' below
$ # Leave the environment: deactivate
```

### Compression

All data is compressed with [zstd](https://github.com/facebook/zstd), make sure it is installed on your system. `Pandas` should recognise `*.csv.zst` files as such and decompress them automatically.

Some system offer packages in their package manager for zstd, e.g.:
* Ubuntu: `sudo apt install zstd libzstd-dev`
* macOS: `brew install zstd`


# How to Reproduce

### Running Jupyter Notbooks

If you follwed the instructions above and you are inside your virtual environment, run `jupyter lab` in this folder. Follow the instructions printed by the terminal and navigate to the given website in your browser. Here you will find the notebooks on the left and can run them individually. In an open a notbook you can run all cells in it via menu entry "Run > Run All Cells".

### Init Data

Run `01-Prepare-Dataframes.ipynb` once and double-check the `./data/pkl` directory for dataframe files.

### Analyse Data

After that, you can simply run any notebook in arbitrary order to reproduce results.
