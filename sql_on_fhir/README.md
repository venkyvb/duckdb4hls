## Testing SQL on FHIR payloads

[FHIR (Fast Health Interoperability Resources)](https://www.hl7.org/fhir/) is an HL7 specification for Healthcare Interoperability (i.e. data exchange between different clinical systems). 

FHIR resources are highly nested JSON payloads. To persist the data we can store the JSON payloads as blobs. Converting the JSON blob to a relational model results in 1000s of tables (depending on the level of normalization needed). The reason for normalization would be to enable querying of the data using SQL.

In this example, we persist the FHIR resources as JSON payloads and then explore the use of DuckDB JSON package to see if we can support [SQL on FHIR](https://github.com/FHIR/sql-on-fhir).
