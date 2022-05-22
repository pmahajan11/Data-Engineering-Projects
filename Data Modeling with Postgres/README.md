# Project: Data Modeling with Postgres

---

## Overview

This repository contains the ETL pipeline for populating the sparkifydb database.

- The goal of this database is to empower Sparkify to answer queries about its customers, the genres of songs people listen to, and the artists that create those songs, using data from logs and files. The database serves as a consistent and dependable repository for this information.

- This data source will be beneficial in assisting Sparkify in achieving some of its analytical objectives, such as identifying songs with the highest appeal or times of day with the highest activity.
---

## ETL Pipeline and Database Schema

- The STAR schema is utilized for schema design because it improves queries and allows rapid data aggregations.
- Python is preferred for the ETL pipeline because it offers packages that simplify data handling, such as Pandas. It also supports Postgres database connections.

- There are two kinds of data involved: song data and log data. It provides information regarding songs and artists, which we extract and load into users and artists dimension tables for song data.

- Log data contains information about each user session. We extract and load log data into time, users dimension tables, and songplays fact tables.
---

## How to run the ETL Pipeline?

1. Execute create tables.py to create the data tables according to the star schema design. Tables that were previously established will be deleted and recreated.

2. Run etl.py to fill the newly constructed data tables.