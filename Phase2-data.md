# Phase 2: Data Understanding

## Data Collection
1. Detail various sources and steps to extract data
- identify data sources and associated platform
    - e.g. object detection training data: vision camera/infrared camera
    - e.g. batch processing v.s. streaming processing?

2. Analyze data for additional requirements
- create awareness of potential data issues
    - e.g. Data encoding/ merging/ obtain more data

3. Consider other data sources
e.g. Online public dataset, customer's domain knowledge.

## Data Properties
1. Describe the data, amount of the data used, and metadata properties
e.g. vision camera data, resolution, length, clips, tables?

2. Find key features and relationships in the data
- structured/unstructured
- relational/un-relational
- needs labeling or not (aws turk, labelimg, out-sourcing)

e.g. object detection requires training data available. data needs to be labelled. 

3. Use tools and techniques to explore data properties
- identify data storage plan:
    - on-prem or cloud
    - data lake or data warehouse
    - what can be stored as relational or which should be stored as key-value
    - e.g. hadoop or regular
    - database modeling
- identify ETL process and related tools for data engineering:
    - e.g. jupyter notebook, snowflake, dataiku, fivetran, spark, etc

## Data Quality
1. Verifying attributes
e.g. if camera data is correctly ingested.

2. Identifying missing data
e.g. if the data of all weather conditions are properly collected? missing data filling.

3. Reveal inconsistencies
e.g. Some of the data with one resolution, other data has another resolution.

4. Report solution
e.g. discard the data with bad resolution.