# Overview

This directory contains additional documentation about our scanning tools.

You do not need to compile or rerun the described tools. We ship all the data to ease reproducability, this means you do not need perform Internet-wide scans.

# QUIC Scans

For our QUIC scans, we use 3 tools:

    1. [quicreach](https://github.com/microsoft/quicreach) changes merged into main.
  2. [QScanner](https://github.com/tumi8/QScanner) as is.
        3. [quiche](https://github.com/josephnoir/quiche) changes still in our own branch, see related markdown file.

# TLS Scans

  1. [openssl](https://github.com/openssl/openssl) as is. As we create CSV files with our own column format, we additionally provide a markdown file with a column description.
  2. [uTLS](https://github.com/refraction-networking/utls) as is.
