## MARC Export Scripts for FOLIO - WORK IN PROGRESS

This code is a work in progress.  It does produce a .mrc file that successfully imports into VuFind.

###What it does
Gets a list of all instance IDs that are not blocked from discovery.
Using the intance ID it looks up the ID for the raw MARC IN the source record storage module
Reads in the MARC record from the database
Attempts to lookup holdings and items for the instance and adds 998 and 097 fields

###What is does not do (yet)
It is not configurable
DB Info is hard-coded
Tenant ID is hard-coded 
Drop records due to encoding ?
Doesn't perform paging or divide the records into multiple files
....things I haven't thought of yet


There are two versions in this repo:

###Java
Works in windows and debian
In my testing on Windows and Debian, encoding issues occur with about 2% of records.  If the ecoding issues cannot be resolved, one possible work-around is constructing the MARC using the JSON in the source record storage.

