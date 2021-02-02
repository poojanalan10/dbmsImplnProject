# dbmsImplnProject

  This script generates data according to the Wisconsin benchmark specification, as described in “The Wisconsin Benchmark: Past, Present, and Future” by David J. DeWitt. In order to follow the benchmark specification as closely as possible, I followed the code laid out in that document and simply ported it to golang. 
We chose POSTGRES SQL beacuse of the exposure to it in the previous courses and the ease of working with a stable system. 
We read the Wisconsin benchamrk paper and learnt how databases can be efficiently benchmarked. 

The following are the two main objectives for the design of Wisconsin benchmark as quoted in the paper.
"The benchmark was designed with two objectives in mind. First, the queries in the benchmark should test the performance of the major components of a relational database system. Second, the semantics and statistics of the underlying relations should be well understood so that it is easy to add new queries and to their behavior."
The benchmark was popular and it set the standard for measuring performanace of various relational database systems at that time and stayed strong with various vendors competing with each other by showing off their commericial database systems.

The following steps demonstrate that we have loaded our data into the postgres system.
1.	Creating a database, databaseuser and connecting to it

CREATE DATABASE dbmsimplnproject;
CREATE USER dbmsimplnprojectuser WITH PASSWORD 'PASSWORD';
GRANT ALL PRIVILEGES ON DATABASE dbmsimplnproject TO dbmsimplnprojectuser;


2.	Creating tables in the database
CREATE TABLE ONEKTUP(unique1 INTEGER UNIQUE NOT NULL, unique2 INTEGER PRIMARY KEY,two INTEGER NOT NULL,four INTEGER NOT NULL,ten INTEGER NOT NULL,twenty INTEGER NOT NULL,onePercent INTEGER NOT NULL,tenPercent INTEGER NOT NULL,twentyPercent INTEGER NOT NULL,fiftyPercent INTEGER NOT NULL,unique3 INTEGER NOT NULL,evenOnePercent INTEGER NOT NULL,oddOnePercent INTEGER NOT NULL,stringu1 CHAR(52) UNIQUE NOT NULL,stringu2 CHAR(52) UNIQUE NOT NULL,string4 CHAR(52) NOT NULL);
 
CREATE TABLE TENKTUP1(unique1 INTEGER UNIQUE NOT NULL,  unique2 INTEGER PRIMARY KEY,two INTEGER NOT NULL, four INTEGER NOT NULL, ten INTEGER NOT NULL, twenty INTEGER NOT NULL, onePercent INTEGER NOT NULL, tenPercent INTEGER NOT NULL, twentyPercent INTEGER NOT NULL, fiftyPercent INTEGER NOT NULL, unique3 INTEGER NOT NULL, evenOnePercent INTEGER NOT NULL, oddOnePercent INTEGER NOT NULL, stringu1 CHAR(52) UNIQUE NOT NULL, stringu2 CHAR(52) UNIQUE NOT NULL,string4 CHAR(52) NOT NULL);

CREATE TABLE TENKTUP2(unique1 INTEGER UNIQUE NOT NULL, unique2 INTEGER PRIMARY KEY,two INTEGER NOT NULL, four INTEGER NOT NULL,ten INTEGER NOT NULL,
twenty INTEGER NOT NULL,onePercent INTEGER NOT NULL,
tenPercent INTEGER NOT NULL,twentyPercent INTEGER NOT NULL,fiftyPercent INTEGER NOT NULL,unique3 INTEGER NOT NULL,evenOnePercent INTEGER NOT NULL,oddOnePercent INTEGER NOT NULL,stringu1 CHAR(52) UNIQUE NOT NULL,stringu2 CHAR(52) UNIQUE NOT NULL,string4 CHAR(52) NOT NULL);
 
3.	Copying the data generated from the script to the tables created in the database.
COPY ONEKTUP FROM '/home/pnalan/dbproject/onektup.csv' WITH (FORMAT csv);
COPY TENKTUP1 FROM '/home/pnalan/dbproject/tenktup.csv' WITH (FORMAT csv);
COPY TENKTUP2 FROM '/home/pnalan/dbproject/tenktup2.csv' WITH (FORMAT csv);
 
4.	Viewing the data copied into the tables.

SELECT * FROM onektup;
SELECT * FROM tenktup1;
SELECT * FROM tenktup2;
 


 

