nexusdb2=# \dx
                                    List of installed extensions
  Name   | Version |   Schema   |                            Description
 
---------+---------+------------+----------------------------------------------
---------------------
pg_trgm | 1.5     | public     | text similarity measurement and index searchi
ng based on trigrams
plpgsql | 1.0     | pg_catalog | PL/pgSQL procedural language
(2 rows)
 
nexusdb2=# select * from pg_extension WHERE extname = 'pg_trgm';
   oid   | extname | extowner | extnamespace | extrelocatable | extversion | ex
tconfig | extcondition
---------+---------+----------+--------------+----------------+------------+---
--------+--------------
1392063 | pg_trgm |    16386 |         2200 | t              | 1.5        |
        |
(1 row)
