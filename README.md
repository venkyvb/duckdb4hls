# duckdb4hls
This is a sample repository that explores the usage of DuckDB for Health & Lifescience use-cases. **Note that this is a work-in-progress repository. Contributions/feedback is welcome !**

## Why DuckDB ?
As described at [DuckDB website](https://duckdb.org/) - DuckDB is an in-process OLAP database. This makes DuckDB a great tool for data scientists, no cloud storage, compute infrastructure needed (other than your own laptop/or a VM on the cloud) to get up and running. DuckDB can be integrated within a Jupyter notebook and with zero-install you can get up and running in no time.  

DuckDB also has a batteries included approach, with (to list a few selected) unique capabilities like - query Parquet, CSV, Arrow and other formats using SQL without doing data imports. Not just query, but query with excellent performance for data-sets that are few 10s to ~100 GB (with a few 10s of millions of records :)) in size. If required, allows direct import of data from CSV, Parquet files, with schema inferencing which simplifies the data engineering process for data scientists. You can run DuckDB as an in-memory engine, with data resident only in-memoty, or persist and load the data from a file. The file can be copied and shared without any dependencies.

This repository contains few example use-cases:
* [Clinical Analytics use-cases](./omop_duckdb/)
* [SQL on FHIR tests](./sql_on_fhir/)