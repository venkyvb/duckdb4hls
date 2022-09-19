# duckdb4hls
This is a sample repository that explores the usage of DuckDB for Health & Lifescience use-cases. **Note that this is a work-in-progress repository. Contributions/feedback is welcome !**

## Why DuckDB ?
As described at [DuckDB website](https://duckdb.org/) - DuckDB is an in-process OLAP database. This makes DuckDB a great tool for data scientists. DuckDB can be integrated within a Jupyter notebook and with zero-install you can get up and running in no time. DuckDB also has a batteries included approach, with (to list a few selected) unique capabilities like - query parquet, CSV and other file formats using SQL without doing data imports. Not just query, but query with excellent performance for data-sets that are few 10s to ~100 GB (with a few 10s of millions of records :)) in size. If required, allows direct import of data from CSV, Parquet files, with schema inferencing which simplifies the data engineering process for data scientists. You can run DuckDB as an in-memory engine or even persist and load the data from a file. The file can be copied and shared without any dependencies.

## Use-cases
Typical use-cases in Health & Lifesciences can be analysis of clinical data.  The first use-case involves:
* Getting clinical data in the form of CSV files, for this purpose we use [Synthea](https://synthetichealth.github.io/synthea/) and download the dataset as CSV archive.
* Clinical data is 'ingested' into DuckDB using CSV import capability.
* Data needs to be harmonized into a common data model for analytics. For this we use the CDM from the [OHDSI OMOP CDM](https://ohdsi.github.io/CommonDataModel/#:~:text=The%20Observational%20Medical%20Outcomes%20Partnership%20%28OMOP%29%20Common%20Data,the%20OMOP%20CDM%20is%20the%20OHDSI%20standardized%20vocabularies). Harmonization involves mapping the clinical data to the OMOP CDM models and also harmonizing the vocabularies. For vocabulary harmonization, download the vocabularies from [OHDSI ATHENA](https://athena.ohdsi.org/). You will have to register for a free account and once activated, you sign-in and follow the options to download the vocabularies. The vocabularies would be in TSV format, which can be directly imported into the CDM for transformation purposes.
* 'Transform' the data (by creating SQL views/tables) from the imported clinical data-sets to the defined CDM models and your are off to races !


