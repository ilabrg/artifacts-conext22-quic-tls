# Artifacts: On the Interplay between TLS Certificates and QUIC Performance



This repository contains the artifacts for the following paper:

    On the Interplay between TLS Certificates and QUIC Performance
    M. Nawrocki, P. F. Tehrani, R. Hiesgen, J. Mücke,  T. C. Schmidt, and M. Wählisch
    In Proceedings of CoNEXT ’22, December 6–9, 2022, Rome, Italy
    ACM, New York, NY, USA, 10 pages
    https://doi.org/10.1145/3555050.3569123



## Structure

We include all data and analysis scripts required to reproduce our results. Additionally, we document our scanning tools. Please see the `README` files in each sub-directory for all details.

This repository is structured as follows:

1. `code/`: Contains Jupyter notebook [code](https://github.com/ilabrg/artifacts-conext22-quic-tls/tree/main/code) to reproduce our results.
2. `data/`: Contains [data](https://github.com/ilabrg/artifacts-conext22-quic-tls/tree/main/data) required by the Jupyter notebooks.
3. `misc/`: Contains additional information on how we performed our [scans](https://github.com/ilabrg/artifacts-conext22-quic-tls/tree/main/misc).



### Minimal Test Setup

Clone this repository, then:

1. Make sure you have Jupyter Notebooks and Python installed.
1. Double-check the Python [requirements](https://github.com/ilabrg/artifacts-conext22-quic-tls/tree/main/code#requirements) and [zstd](https://github.com/facebook/zstd).
1. Prepare the analysis by running the initial notebook [01-Prepare-Dataframes.ipynb](https://github.com/ilabrg/artifacts-conext22-quic-tls/blob/main/code/01-Prepare-Dataframes.ipynb) once.
1. Run all the other notebooks in arbitrary order, *i.e.,* from [02-Section-4.1-Classify-Handshakes.ipynb](https://github.com/ilabrg/artifacts-conext22-quic-tls/blob/main/code/02-Section-4.1-Classify-Handshakes.ipynb) up to [08-Addendum-Rescan-Confirm-CertReuse.ipynb](https://github.com/ilabrg/artifacts-conext22-quic-tls/blob/main/code/08-Addendum-Rescan-Confirm-CertReuse.ipynb). If RAM is limited, remember to shutdown notebook kernels after you are done with a notebook.
1. Find all results in `./code/plots/`, located [here](https://github.com/ilabrg/artifacts-conext22-quic-tls/tree/main/code/plots) or directly in the notebooks.
