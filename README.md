# Basic Eastmoney Guba posting records

This package contains a minimal, de-identified projection of the locally retained Eastmoney Guba crawler CSV files. It is intended as source data for the study of shared-poster stock networks.

## Download

Download the [v1.0.0 data archive](https://github.com/lijy8956-beep/shared-poster-stock-data/releases/download/v1.0.0/guba_basic_data_20261024.zip) from the [release page](https://github.com/lijy8956-beep/shared-poster-stock-data/releases/tag/v1.0.0). Select `guba_basic_data_20261024.zip`; the automatically generated GitHub source-code archives contain repository documentation only.

- Archive size: 157,077,841 bytes.
- SHA-256: `6912a2d93d5500884417e85ddb6b9132a1efbe0764857ee0786f837a30867abc`.
- Extract the ZIP, then read or decompress the `posts/*.csv.gz` files. Both README.md and file_manifest.csv are included in the archive.

## Coverage

- Source files: 999, one per stock.
- Stock codes in these source records: 999.
- Posting records: 10,826,065.
- Timestamp range: 2024-07-01 00:00:00 to 2025-08-31 23:59:58.
- Distinct nonempty source poster identifiers: 1,043,649.
- Records with an empty source poster identifier: 0.

These are collected records before the manuscript's stock-universe and record-cleaning steps. The manuscript models a fixed set of 959 stocks. The source-file coverage must not be interpreted as the final analytical sample.

## Files and fields

Each `posts/*.csv.gz` file is a gzip-compressed UTF-8 CSV. `file_manifest.csv` records the number of records, byte size, and SHA-256 checksum of every data file.

| Field | Meaning |
| --- | --- |
| stock_code | Stock code from the original crawler CSV; read as text to retain leading zeros. |
| poster_id | Consistent pseudonym of the original author identifier. The same source identifier maps to the same pseudonym across all stocks and dates. Empty identifiers remain empty. |
| read_num | Original collected read-count field, retained as recorded. |
| comment_num | Original collected comment-count field, retained as recorded. |
| publish_time | Original collected posting timestamp, retained as recorded. |

The nickname, original account identifier, stock-name text, and post-title text are omitted. No posting records are deduplicated, removed, re-dated, or aggregated in this export. No counts are normalized. The pseudonym mapping and secret key are not included in this package.

The locally retained folder was named `data_corrected`; this package does not claim to be an untouched HTTP response archive. Read and comment counts represent collected snapshots and are not certified as values available at the original posting time.

This package contains posting records and documentation only. It does not contain model files, graphs, predictions, backtest outputs, manuscript files, credentials, or Tushare market data. No new license is asserted over third-party source material.
