[comment]: # "Auto-generated SOAR connector documentation"
# InfluxDB

Publisher: Irek Romaniuk  
Connector Version: 1\.0\.4  
Product Vendor: InfluxData  
Product Name: InfluxData  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.251  

This app implements various investigative actions against an InfluxDB instance


InfluxDB is a time series database meant to be used as a backing store for any use case involving
large amounts of timestamped data, including DevOps monitoring, application metrics, IoT sensor
data, and real-time analytics.


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a InfluxData asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base\_url** |  required  | string | InfluxDB endpoint
**verify\_cert** |  optional  | boolean | Verify Server Certifcate
**username** |  optional  | string | Username
**password** |  optional  | password | Password
**db** |  optional  | string | Target Database

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[run query](#action-run-query) - Run a query on InfluxDB  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'run query'
Run a query on InfluxDB

Type: **investigate**  
Read only: **False**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**query** |  required  | query | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.query | string | 
action\_result\.data | string | 
action\_result\.data\.\*\.results | string | 
action\_result\.data\.\*\.results\.\*\.series | string | 
action\_result\.data\.\*\.results\.\*\.series\.\*\.values | string | 
action\_result\.data\.\*\.results\.\*\.series\.\*\.name | string | 
action\_result\.data\.\*\.results\.\*\.series\.\*\.columns | string | 
action\_result\.summary | string | 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 