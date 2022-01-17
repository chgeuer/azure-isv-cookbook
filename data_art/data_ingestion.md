
# Data Ingestion

The document would focus on data lake ingestion.

## Disclaimer

“FastTrack for Azure" are “Professional Services” provided free of charge subject to the “Professional Services Terms” in the Online Services Terms and Online Services Data Protection Addendum.
This document is provided “AS-IS,” WITHOUT WARRANTY OF ANY KIND. Microsoft disclaims all express, implied or statutory warranties, including warranties of quality, title, non-infringement, merchantability and fitness for a particular purpose.

## Context

Data ingestion is defined as the process of collecting and saving data.

Large quantities of data should be saved to [Hierarchal storage account](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-namespace)_.
Data premise is considered any and all data repositories you might have, storage accounts, disks, databases etc.
It is highly recommended to anonymize any and all PII data reaching your data premise.

## Data Sources

First, lets outline potential data sources, and review relevant ingestion methods per source type.

- Publicly available - This pertain to any data which is available to consume, it does not contain any PII data, and is assumed to be transient in a way that if lost - it can be obtained again, and no significant risk is created due to it being deleted.

- Customer data - Data which is owned by CMV's customers. It is considered confidential. There is no PII data as part of it.

- PII - This document assume no PII data is part of the data estate.
TODO: add reference to PII related concepts.

## Ingestion Methods

In both methods described it is recommended to use linkd to the data and not the actual data. This is primarily due to size limitation and the fact the receiving application would be required to buffer the data and then save it to a persistent storage.  (lake)
Couple of ingestion concepts:

- Pull - A request is made to the source of data. The pull can be of the actual data, or a link to the actual location of the data.

- Push - The source of data is calling the target to notify of new data availability (link to the new data) or the actual data.

It is highly recomended to confirm with the ISV customers, what can be the most convinient way of sending data. Customers might be able to provide storage location, actual files, or in other cases byte streams. While few customers might find your approach new or diffrent, providing the customer with sample code might ease or prevent friction.

### Batch vs. Stream

Streaming of data is required in some specific use cases, where the data freshness is crucial to the business. Real-time or near real-time decision making and billing calculation are two potential scenarios, however they should not be created on a data lake.
In most scenarios data ingestion to data lake batch processing would be sufficent, given some data sources might be emmiting data in stream, thus requiring the lake to be able and accept it. Having said that, continuance data ingestion is not equivalent to streaming.
