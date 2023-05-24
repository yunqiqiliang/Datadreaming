# Clickzetta

This page guides you through the process of setting up the [Clickzetta](https://yunqi.tech/) destination connector.

## Features
Clickzetta Lakehouse destination supports the following sync modes:

| Feature | Supported?\(Yes/No\) | Notes |
| :--- | :--- | :--- |
| Full Refresh - Overwrite | Yes |  |
| Full Refresh - Append | Yes |  |
| Incremental - Append Sync | Yes |  |
| Incremental - Deduped History Sync | Yes |  |

#### Output Schema

Each stream will be output into its own table in Databend. Each table will contain 3 columns:

* `_airbyte_ab_id`: a uuid assigned by Airbyte to each event that is processed. The column type in Databend is `VARCHAR`.
* `_airbyte_emitted_at`: a timestamp representing when the event was pulled from the data source. The column type in Databend is `TIMESTAMP`.
* `_airbyte_data`: a json blob representing with the event data. The column type in Databend is `VARVHAR`.

## Getting Started (Airbyte Open-Source)
You can follow the [Connecting to a Warehouse docs](https://yunqi.tech/) to get the user, password, host etc.

#### Target Database

You will need to choose an existing database or create a new database that will be used to store synced data from Airbyte.

### Setup the Clickzetta Destination in Airbyte

You should now have all the requirements needed to configure Databend as a destination in the UI. You'll need the following information to configure the Clickzetta destination:

* **Host**
* **Virtual Cluster**
* **Database Name**
* **Default Schema**
* **Username**
* **Password**

## Compatibility


## Changelog

| Version | Date       | Pull Request                                             | Subject                                         |
|:--------|:-----------|:---------------------------------------------------------|:------------------------------------------------|
| 0.1.2   | 2023-05-24 | demo | Demo |



