
# Data Ingestion

It is highly recomended to review our architecture center content and specificly the items [related to data](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-data).

The document would focus on data lake ingestion.

## Disclaimer

"FastTrack for Azure" are "Professional Services" provided free of charge subject to the "Professional Services Terms" in the Online Services Terms and Online Services Data Protection Addendum.
This document is provided "AS-IS", WITHOUT WARRANTY OF ANY KIND. Microsoft disclaims all express, implied or statutory warranties, including warranties of quality, title, non-infringement, merchantability and fitness for a particular purpose.

## Context

Data ingestion is defined as the process of collecting and saving data.
The reference architecture and content for [the retail view](https://docs.microsoft.com/en-us/previous-versions/azure/industry-marketing/retail/retail-data-management-overview?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Farchitecture%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Farchitecture%2Fbread%2Ftoc.json) is one of the best starting points.
Large quantities of data should be saved to [Hierarchal storage account](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-namespace).
Data premise is considered any and all data repositories you might have, storage accounts, disks, databases etc.
It is highly recommended to anonymize any and all PII data reaching your data premise.

## Data Sources

First, lets outline potential data sources, and review relevant ingestion methods per source type. The industry uses the 3Ps:

- Public - open and avilable for all.
- Purchased - avilable for a fee.
- Propitery - the data you create.

## Ingestion Methods

In both methods described it is recommended to use links to the data and not the actual data. This is mainly due to size limitation and the fact the receiving application would be required to buffer the data and then save it to a persistent storage.  (lake)
Couple of ingestion concepts:

- Pull - A request is made to the source of data. The pull can be of the actual data, or a link to the actual location of the data.
- Push - The source of data is calling the target to notify of new data availability (link to the new data) or the actual data.

It is highly recomended to confirm with the ISV customers, what can be the most convinient way of sending data. Customers might be able to provide storage location, actual files, or in other cases byte streams. While few customers might find your approach new or diffrent, providing the customer with sample code might ease or prevent friction.

### ETL vs. ELT

Not too long ago, it was custom to perform Extraction (bringing the data) Transformation (manipulate the data) and Load (save to a destination). Given that one cannot know at the early stages of a project, what other transformation might be needed, or what other insights the same data might provide, it is now more common to leverage the Extract - Load (to the lake) and then transform.

### Batch vs. Stream

Streaming of data is required in some specific use cases, where the data freshness is crucial to the business. Real-time or near real-time decision making and billing calculation are two potential scenarios, however they should not be created on a data lake.
In most scenarios data ingestion to data lake batch processing would be sufficent, given some data sources might be emmiting data in stream, thus requiring the lake to be able and accept it. Having said that, continuance data ingestion is not equivalent to streaming.

## Data stores

As mentioned using [Hierarchal storage account](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-namespace) should be your default choice for storing large quantities of data.
The most common practice of storing data is using the:

- Bronze - raw, unfiltered data
- Silver - cleansed and filtered
- Gold - your buisness level data (e.g. aggregations)

When adopting this practice, each area is a [container](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction#containers).

## Orchestration

Using [Azure Data Factory](https://docs.microsoft.com/en-us/azure/data-factory/introduction) is the recomended approach.
Data factory has multiple buil-in connectors, and is able to call most of the transformation options, the load proceeses.

## Transformations

There are few options which are essentialy determined by the level and type of skilling and the varaity of data. Transformation can be as minimal as formatting dates, to complicated data aggregation.

- [Data Flow](https://docs.microsoft.com/en-us/azure/data-factory/concepts-data-flow-overview) - provide straigt forward development
- [Synapse Serverless](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql/on-demand-workspace-overview) - can connect to your lake and provide SQL like access.
- [Synapse Spark Pool](https://docs.microsoft.com/en-us/azure/synapse-analytics/spark/apache-spark-overview) - in case spark is your forte
- [Databricks](https://docs.microsoft.com/en-us/azure/databricks/) - when you want to use the latest, rich platform and you eat spark for breakfast.
