 Testing Certificate Compression Support using Quiche

[Quiche](https://github.com/cloudflare/quiche) is a QUIC implementation maintained by Cloudflare. It uses BoringSSL for cryptography. The implementation comes with support for certificate compression with Brotli. [We forked](https://github.com/josephnoir/quiche) and extended the project to add zlib and zstd support as well as flags to choose with algorithms to enable. During the handshake the tool prints the size of the certificate before and after decompression.

## Building

The fork has a branch with all our changed. Clone it, checkout the branch (`josephnoir/compression-with-print`), and build it as follows:

```bash
# git clone --recursive https://github.com/josephnoir/quiche
# cd quiche
# git checkout josephnoir/compression-with-print
# cargo build --release
```

## Usage

The binary is then located at `./target/release/quiche-client`. To run it against websites a few options are helpful:

```
--wire-version=1 # Set the QUIC version to 1.
--comp-algo=ALGO # Algo can be zlib, brotli, or zstd. Per default all of them are enabled.
```

The output will be mangled in with the website content. To make the output easier to parse we print CSV-lines that use `|` as the separator. The first column always contains `++` to make these lines easy to filter out using grep, the second column contains the name of the compression algorithm and the last two columns contain the input length (before decompression) and the final length.
