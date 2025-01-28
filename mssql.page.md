# MSSQL Enumeration #

- Schema Enumeration
`select * from INFORMATION_SCHEMA.SCHEMATA;`

- Table Enumeration
`select TABLE_NAME from INFORMATION_SCHEMA.TABLES;`

- Column Enumeration
`select * from INFORMATION_SCHEMA.COLUMNS;`

- Role Enumeration
`SELECT name FROM sys.database_principals WHERE type = 'R;`

- Stored Procedure Enumeration
`SELECT name FROM sys.procedures;`

- Version
`SELECT @@VERSION;`

- Linked Servers
`SELECT * FROM sys.servers;`

- Sensitive Data
`SELECT name FROM sys.tables WHERE name LIKE '%password%' OR name like '%secret%'`


