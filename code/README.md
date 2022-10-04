All Jupyter notebooks can be found in this directory.

# Requirements

We tested these artifacts with `Python 3.10` with the following additional requirements:

```
numpy
pandas
matplotlib
seaborn
```

### Compression

All data is compressed with [zstd](https://github.com/facebook/zstd), make sure it is installed on your system. `Pandas` should recognise `*.csv.zst` files as such and decompress them automatically.



# How to Reproduce

### Init Data

Run `01-Prepare-Dataframes.ipynb` once and double-check the `./data/pkl` directory for dataframe files.

### Analyse Data

After that, you can simply run any notebook in arbitrary order to reproduce results.
