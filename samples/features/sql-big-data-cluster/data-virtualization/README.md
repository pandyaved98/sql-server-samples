# Data virtualization in SQL Server 2019 big data cluster

In SQL Server 2019 big data clusters, the SQL Server engine has gained the ability to natively read HDFS files, such as CSV and parquet files, by using SQL Server instances collocated on each of the HDFS data nodes to filter and aggregate data locally in parallel across all of the HDFS data nodes. SQL Server 2019 introduces new ODBC connectors to data sources like SQL Server, Oracle, MongoDB and Teradata.

## Query data in HDFS from SQL Server master

In this example, you are going to create an external table in the SQL Server Master instance that points to data in HDFS within the SQL Server Big data cluster. Then you will join the data in the external table with high value data in SQL Master instance.

### Instructions

1. Connect to SQL Server Master instance.

1. Execute the [external-table-hdfs.sql](external-table-hdfs.sql).

## Query data in Oracle from SQL Server master

In this example, you are going to create an external table in SQL Server Master instance over the inventory table that sits on an Oracle server.

**Before you begin**, you need to have an Oracle instance and credentials. Execute the SQL script [inventory-ora.sql](inventory-ora.sql/) in Oracle to create the table and import the "inventory.csv" file created by the bootstrap sample database.

### Instructions

1. Connect to SQL Server Master instance.

1. Execute the SQL [external-table-oracle.sql](external-table-oracle.sql/).