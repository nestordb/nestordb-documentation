# NestorDB - Documentation

## Loading data
You can download the following datasets: 
- [datafile](https://github.com/nestordb/nestordb-documentation/blob/master/sim.csv?raw=true)
- [metadata file](https://github.com/nestordb/nestordb-documentation/blob/master/sim-metadata.csv?raw=true)

To insert the data in the database use the following command:
``python
>>> from client import TStoreClient
>>> cl = TStoreClient("127.0.0.1", 8690)
>>> cl.query("CREATE DATABASE db1;")
>>> cl.query("CREATE TABLE db1.tbl1 ($position UInt64C, ~value Double, sensorid VarChar64);")
>>> cl.query("LOAD \"/home/kostas/projects/nestor/core/data/sim/sim.csv\" \"/home/kostas/projects/nestor/core/data/sim/sim.metadata.csv\" INTO db1.tbl1;")


