
# Db2 Internals

SQL statements can be inserted into source application programs. This type of invocation is referred to as an embedded statement. 
* COBOL EXEC SQL is how you use a sql embedded statement closed with END-EXEC
* Similar to process for C and C++ programs close with semicolon
* Java use a #sql and close with semicolon


With static SQL statements the Db2 precompiler or coprocessor checks the sysntax of SQL statements and will convert them into host language statemnts that are used to access Db2 data

Dynamic sql statements must be processed at runtime
Db2 precompiler stage producues Database request moduel that contains SQL statmenets

SQL statements can be sent direclty using TSO facilty called SPUFI(SQL processor using file input)

XML data can be stored in a Db2 tabe Db2 usess feature called pureXML data stored in Db2 tables

JSON is now supported in Db2 v10

All tables within Db2 are stored in table spaces which is a storage structure that consists of SAM data sets. Table spaces can be created by issuing a CREATE TABLESPACE command or Db2 automatically when a table is created.


Tables oftentimes have unique keys, they also have primary keys which are unique keys that cannot be null

View is segmented part of the table to not share more information than needed

Storage groups
: Area on a disk used to store tables and indexes

Schemaa
: Used to group sets of objects within the Db2 databse together using high-levle qualifies names. They consist of indexs and table spaces, functions, stored porcedures, and triggers

Linking data together forms a database. Allows operators to combine data felxibly with permissions and masking non relavent/sensitive information