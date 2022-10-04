All raw, compressed CSV files. Large files have been split up into chunks to avoid file limits.

These files will be loaded, parsed, sanitized, potentially merged and finally dumped as a dataframe in the `pkl` folder.



1. `https_parsed_certs_chunk_*.csv.zst` CSV chunks with TLS information from TCP/HTTPS scans.
2. `quicreach_handshakes_chunk_0.csv.zst` CSV chunks with QUIC handshake information for all QUIC services.
3. `qscanner_tls_cert_hashes.csv.zst` CSV containing TLS information received over QUIC.
4. `quiche_tls_compression.csv.zst` CSV containing information about supported compression algorithms over QUIC.
5. `backscatter_cdf_ampl_factor_hypergiants.csv.zst` CSV containing CDF data for backscatter traffic. More precise data not released due to NDAs.
6.  `tranco_Q9QQ4-top-1m.csv.zst` recompressed tranco list.
7. `https_parsed_certs_rescan.csv.zst` data from a rescan with our TCP/HTTPS tools to double-check for certificate roll-overs.

