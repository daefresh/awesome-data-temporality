# Awesome Data Temporality
> A curated list to help you manage temporal data across many modalities 🚀.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<img src="data-temporality-header.png" width="300">

Generative Art Created By DALL·E!

- [Awesome Data Temporality](#awesome-data-temporality)
  - [Data Versioning for Machine Learning](#data-versioning-for-machine-learning)
  - [Time Travel and Temporal Tables](#time-travel-and-temporal-tables)
  - [Slowly Changing Dimensions Data Modeling](#slowly-changing-dimensions-data-modeling)
  - [Bi-temporality Tools + Modeling](#bi-temporality-tools--modeling)
  - [Change Data Capture (CDC) Tools](#change-data-capture-cdc-tools)
  - [Soft Delete in ORM Frameworks](#soft-delete-in-orm-frameworks)
  - [Contribution](#contribution)

## Data Versioning for Machine Learning
Data versioning is the practice of storing multiple versions of the same data and providing a mechanism for accessing and managing these versions. This can be useful in a variety of situations, such as when data is accidentally deleted or corrupted, or when it is necessary to see how the data has changed over time. The vast majority of "data versioning" tools you see today are related to better managing your datasets for machine learning. The implementation paradigm used is to store versions of your data and models in Git commits. Therefore the following part of the awesome list is centered around machine learning. However, there are other ways to manage your temporal data covered in later sections.

- [DVC](https://dvc.org/doc/use-cases/versioning-data-and-models) Management and versioning of datasets and machine learning models.
- [lakeFS](https://lakefs.io/) Repeatable, atomic and versioned data lake on top of object storage.
- [Dolt](https://github.com/dolthub/dolt) Dolt is Git for Data!
- [Pachyderm](https://www.pachyderm.com/) Pachyderm data versioning technology 
- [wrgl](https://www.wrgl.co/) Data version control for data projects
- [neptune](https://neptune.ai/) Log, organize, compare, register, and share all your ML model metadata in a single place
- [Git LFS](https://git-lfs.com/) An open source Git extension for versioning large files
- [DagsHub](https://dagshub.com/) Where people build data science projects
- [Neptune](https://neptune.ai/blog/best-data-version-control-tools) Best 7 Data Version Control Tools
- [DagsHub](https://dagshub.com/blog/data-version-control-tools/) Comparing Data Version Control Tools
- [Aporia](https://www.aporia.com/blog/best-data-version-tools-for-mlops-2021/) Best Data Versioning Tools for MLOps
- [A Conceptual Framework](https://www.researchgate.net/publication/350325954_Versioning_Data_Is_About_More_than_Revisions_A_Conceptual_Framework_and_Proposed_Principles) A Conceptual Framework and Proposed Principles
- [Australian Research Data Commons](https://ardc.edu.au/resource/data-versioning/) What is data versioning?
- [Research Data Alliance](https://www.rd-alliance.org/group/data-versioning-wg/outcomes/principles-and-best-practices-data-versioning-all-data-sets-big) Principles and best practices in data versioning for all data sets big and small
- [MLFlow + LakeFS](https://medium.com/towards-artificial-intelligence/data-versioning-for-efficient-workflows-with-mlflow-and-lakefs-892df1f8e7d8) Data Versioning for Efficient Workflows with MLFlow and LakeFS
- [LakeFS](https://towardsdatascience.com/data-versioning-all-you-need-to-know-7077aa5ed6d1) Data Versioning: All You Need to Know
- [Dr. Raj Ramesh](https://www.youtube.com/watch?v=LQF6vHm_QIY) How to manage model and data versions
- [DVC + MLflow (DVC)](youtube.com/watch?v=W2DvpCYw22o) Data Versioning and Reproducible ML with DVC and MLflow
- [5 min Explainer (DVC)](https://www.youtube.com/watch?v=UbL7VUpv1Bs) Version Control for Data Science Explained in 5 Minutes
- [The Guide to Data Versioning (LakeFS)](https://medium.com/whispering-data/the-guide-to-data-versioning-d4315a146456) The Guide to Data Versioning with LakeFS
- [CodeX](https://medium.com/codex/data-versioning-for-modern-data-teams-and-platforms-86e8bba14f14) Data Versioning for Modern Data Teams and Platforms Advantages & Best Practices
- [DevGenius](https://medium.com/dev-genius/fundamentals-of-data-versioning-you-must-know-647a12102635) Data versioning applied on machine learning projects
- [Eduonix Data Versioning](https://blog.eduonix.com/bigdata-and-hadoop/data-versioning-how-to-version-your-data/) Data Versioning - How to Version your Data
- [DZone Data Versioning](https://dzone.com/articles/data-versioning-101) Data Versioning 101
- [KDNuggets Data Versioning](https://www.kdnuggets.com/2020/08/data-versioning-mean-think-means.html) Data Versioning: Does it mean what you think it means?
- [ODSC Data Versioning](https://opendatascience.com/how-data-versioning-can-be-used-in-machine-learning/) How Data Versioning Can Be Used in Machine Learning
- [Neuroimaging (Quilt)](https://medium.com/quilt/use-cases-for-data-versioning-debugging-collaboration-and-compliance-in-neuroimaging-webinar-7e9a2e7a2e7c) Use cases for data versioning: debugging, collaboration, and compliance in neuroimaging
- [Data + AI Summit Europe 2020 (DVC)](https://www.databricks.com/session_eu20/data-versioning-and-reproducible-ml-with-dvc-and-mlflow) Data Versioning and Reproducible ML with DVC and MLflow


## Time Travel and Temporal Tables
Data time travel refers to the ability to go back in time and access previous versions of data. In order to enable data time travel, it is necessary to implement a system for versioning data, which involves storing multiple versions of the same data and providing a mechanism for accessing and managing these versions. Whereas temporal tables, also known as system-versioned temporal tables, are tables in a database that automatically track the history of data changes and allow you to query the data as it existed at any point in time. Both time travel an temporal tables often are used interchangablely to mean the same thing. Temporal tables are more of an implementation specific feature of some databases. These tables are useful for auditing, tracking changes to data over time, and performing point-in-time analysis. You can usually query a temporal table using the FOR SYSTEM_TIME clause in a SELECT statement. 

- [Postgres](https://pgxn.org/dist/temporal_tables/) Postgres Temporal Tables Extension
- [Azure](https://learn.microsoft.com/en-us/sql/relational-databases/tables/temporal-tables?view=sql-server-ver16) MSSQL temporal tables
- [MariaDB](https://mariadb.com/kb/en/temporal-tables/) MariaDB Temporal Tables
- [Cockroach](https://www.cockroachlabs.com/docs/stable/as-of-system-time.html) Cockroach documentation about AS OF SYSTEM TIME
- [Dremio](https://www.dremio.com/resources/guides/apache-iceberg-an-architectural-look-under-the-covers/#toc_item_Time%20Travel) Dremio Iceberg Time Travel
- [Iceberg](https://iceberg.apache.org/docs/latest/spark-queries/#time-travel) Apache iceberg time travel
- [Teradata](https://www.docs.teradata.com/r/Teradata-VantageTM-Temporal-Table-Support/March-2019/Getting-Started/Temporal-Statements/Related-Information) Teradata Vantage™ Temporal Table Support
- [SAP HANA](https://help.sap.com/docs/SAP_HANA_PLATFORM/6b94445c94ae495c83a19646e7c3fd56/cf3523ab01834f5e84a32164c1fd597a.html) Temporal Tables (History, System-Versionined, Application-Time Period)
- [Delta Lake](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-qry-select.html#as-of-syntax) Introducing Delta Time Travel for Large Scale Data Lakes
- [Hopsworks](https://examples.hopsworks.ai/master/featurestore/hsfs/time_travel/time_travel_python/) Time travel operations in Hopsworks Feature Store
- [BigQuery](https://cloud.google.com/bigquery/docs/time-travel) Access historical data using time travel
- [JOOQ](https://www.jooq.org/doc/latest/manual/sql-building/table-expressions/temporal-tables]) System and application versioned tables
- [Apache Flink](https://nightlies.apache.org/flink/flink-docs-release-1.16/docs/dev/table/concepts/temporal_table_function/) Temporal Table Function
- [Apache Arrow](https://voltrondata.com/resources/apache-arrow-version-9-0-0-released) Voltron as-of join (not exactly bi-temporal, but is temporal joining)
- [Redpanda](https://redpanda.com/blog/redpanda-22-2-announcement) Time travel debugging through historical messages to identify and debug problems
- [Time Travel or Data Versioning (DataBricks)](https://www.youtube.com/watch?v=BJDgxfoVHDA) Time Travel/Data Versioning using Delta Lake
- [Data Reproducibility (DataBricks)](https://www.youtube.com/watch?v=g2mdSPISmG4) Data Reproducibility, Audits, Immediate Rollbacks, and Other Applications of Time Travel
- [Apache Iceberg (Trino)](https://www.youtube.com/watch?v=ifXpOn0NJWk) Apache Iceberg: A table format for data lakes with unforeseen use cases
- [Hopworks Point-in-time Joins](https://www.youtube.com/watch?v=AIof4woJSkY) Python-centric Feature Stores
- [Iceberg Architecture](https://www.youtube.com/watch?v=N4gAi_zpN88) Data Science DC Nov 2021 Meetup: Apache Iceberg - An Architectural Look Under the Covers
- [Postgres - Paper](https://www.researchgate.net/publication/290429619_Temporal_Data_Time_Travel_in_PostgreSQL) Temporal Tables in Postgres
- [MSSQL (Business Problems)](https://www.youtube.com/watch?v=VUuWWm66NQM) 5 Business Problems You Can Solve Using Temporal Tables
- [MSSQL (Tim Mitchell)](https://www.youtube.com/watch?v=BsGJlJ06dcI) Introduction to SQL Server Temporal Tables Tim Mitchell


## Slowly Changing Dimensions Data Modeling
Slowly changing dimensions are those in which the attributes of the dimension change over time, and the changes need to be tracked in the data warehouse. For example, a customer's address or name might change over time, and the data warehouse needs to track these changes so that historical data can be analyzed correctly. 

- [VDK](https://github.com/vmware/versatile-data-kit) Versatile Data Kit (VDK) is an open source framework including help to manage SCD style data.
- [dbtvault](https://github.com/Datavault-UK/dbtvault) A free to use dbt package for creating and loading Data Vault 2.0 compliant Data Warehouses (powered by dbt, an open source data engineering tool, registered trademark of dbt Labs)
- [dataform](https://github.com/dataform-co/dataform-scd) Common data models for creating type-2 slowly changing dimensions tables from mutable data sources in Dataform.
- [dbt snapshots](https://docs.getdbt.com/docs/build/snapshots) DBT snapshots
- [DeltaLake](https://docs.databricks.com/workflows/delta-live-tables/delta-live-tables-cdc.html) Databricks change data capture with Delta Live Tables
- [6 Kinds](https://medium.com/geekculture/6-different-types-of-slowly-changing-dimensions-and-how-to-apply-them-b152ef908d4e) 6 Different Types of Slowly Changing Dimensions and How to Apply Them?
- [Data Vault](https://danischnider.wordpress.com/2015/11/12/loading-dimensions-from-a-data-vault-model/) Loading Dimensions from a Data Vault Model
- [SCD Data Warehouse](https://www.researchgate.net/publication/332152952_Slowly_Changing_Dimension_Handling_in_Data_Warehouses_Using_Temporal_Database_Features) Slowly Changing Dimension Handling in Data Warehouses Using Temporal Database Features
- [Redshift](https://aws.amazon.com/blogs/big-data/implement-a-slowly-changing-dimension-in-amazon-redshift/) Implement a slowly changing dimension in Amazon Redshift


## Bi-temporality Tools + Modeling
Bitemporality is a concept in database management that refers to the ability of a database to store and manage data that is associated with multiple time periods. This can include historical data as well as data that is still in the process of being entered or updated. In a bitemporal database, data is stored in multiple versions, with each version corresponding to a specific point in time. This allows users to view and query the data as it existed at different points in time, which can be useful for a variety of purposes such as understanding how data has changed over time or for tracking the history of a particular piece of data.

- [Martin Fowler](https://martinfowler.com/articles/bitemporal-history.html) Bitemporal History (explained) from world famous Martin Fowler
- [Crux of Bitemporality](https://www.youtube.com/watch?v=3Stja6YUB94) The Crux of Bitemporality - Jon Pither
- [Capgemini](https://www.capgemini.com/ch-en/wp-content/uploads/sites/43/2017/07/Enhancing_Time_Series_Data_by_Applying_Bitemporality.pdf) Enhancing Time Series Data by Applying Bitemporality (opinionated white paper mentioning KDB+)
- [GoldenSource](https://www.thegoldensource.com/bitemporal-data-preserving-moment-time/) A financial services data modeling software company perspective on bitemporality
- [MarkLogic](https://www.marklogic.com/blog/bitemporal/) A deep dive into bitemporality in MarkLogic
- [XTDB](https://docs.xtdb.com/concepts/bitemporality/) XTDB bitemporal graph database by Juxt with support for bitemporality
- [ARXIV](https://arxiv.org/pdf/2111.13499.pdf) Bitemporal Property Graphs to Organize Evolving Systems white paper
- [Axway](https://docs.axway.com/bundle/DecisionInsight_LATEST_allOS_en_HTML5/page/bi-temporality.html) Decision Insights bitemporal capability
- [Cloudera - Data Modeling](https://blog.cloudera.com/bi-temporal-data-modeling-with-envelope/) Bi-temporal data modeling with Envelope
- [Bitemporal Database Book](https://www.amazon.com/Bitemporal-Databases-Canan-Eren-Atay/dp/3639131878) Bitemporal Databases: Modeling and Implementation
- [Speakerdeck](https://speakerdeck.com/krivachy/an-overview-of-bitemporality?slide=32) An overview of bitemporality
- [Val on Programming (Datomic)](https://vvvvalvalval.github.io/posts/2017-07-08-Datomic-this-is-not-the-history-youre-looking-for.html) Datomic: this is not the history you're looking for
- [Cybertec](https://www.cybertec-postgresql.com/en/implementing-as-of-queries-in-postgresql/) Implementing "As Of" queries in Postgresql
- [Bitempura.DB](https://github.com/elh/bitempura) Bitempura.DB is a simple, bitemporal key-value database.
- [Modeler (Anchormodeler)](https://github.com/eliask/modeler) (Bi-temporal) data modelling tool inspired by Anchor modeler, for PostgreSQL
- [BarbelHisto](https://github.com/projectbarbel/barbelhisto-core) Lightweight ultra-fast Java library to store data in bi-temporal format
- [Robinhood](https://robinhood.engineering/tracking-temporal-data-at-robinhood-b62291644a31) Tracking Temporal Data at Robinhood


## Change Data Capture (CDC) Tools
Change data capture (CDC) is a process that captures and stores data about changes made to a database or other data source. It is often used in data warehousing and data integration scenarios to ensure that data in different systems is kept up to date and in sync. CDC involves tracking changes made to a database or data source and storing information about those changes in a separate location, such as a separate database or log file. This allows the data in the original source to be updated, while still maintaining a record of the changes that were made.

- [Debezium](https://github.com/debezium/debezium) Change data capture for a variety of databases
- [Supabase realtime](https://github.com/supabase/realtime) Broadcast, Presence, and Postgres Changes via WebSockets
- [airbyte](https://github.com/airbytehq/airbyte) Data integration platform for ELT pipelines from APIs, databases & files to warehouses & lakes
- [Flink](https://github.com/ververica/flink-cdc-connectors) CDC Connectors for Apache Flink
- [gravity](https://github.com/moiot/gravity) A Data Replication Center
- [brooklin](https://github.com/linkedin/brooklin) An extensible distributed system for reliable nearline data streaming at scale


## Soft Delete in ORM Frameworks
Soft delete is a method of deleting data from a database in a way that allows the data to be recovered if necessary. When data is deleted using the soft delete method, it is not physically removed from the database. Instead, it is marked as deleted and is typically no longer visible to users, but it can still be recovered if necessary. The soft delete method is often used as a way to prevent accidental or unintended data loss, as it allows deleted data to be recovered if necessary. It is also useful in scenarios where data needs to be retained for compliance or regulatory purposes, as it allows data to be retained while still making it unavailable to users.

- [Golang Bun](https://bun.uptrace.dev/guide/soft-deletes.html#introduction) Lightweight Golang ORM for PostgreSQL, MySQL, MSSQL, and SQLite
- [Golang GORM](https://gorm.io/docs/delete.html#Soft-Delete) The fantastic ORM library for Golang
- [Typescript DeepKit](https://docs.deepkit.io/english/database.html#_plugins) High performance typescript framework
- [Java Spring](https://www.baeldung.com/spring-jpa-soft-delete) How to Implement a Soft Delete with Spring JPA
- [Typescript TypeOrm](https://doug-martin.github.io/nestjs-query/docs/persistence/typeorm/soft-delete/) Easy CRUD for GraphQL
- [Typescript Sequalize](https://sequelize.org/docs/v6/core-concepts/paranoid/) Sequelize is a modern TypeScript and Node.js ORM for Oracle, Postgres, MySQL, MariaDB, SQLite and SQL Server, and more.
- [Typescript Prisma](https://www.prisma.io/docs/concepts/components/prisma-client/middleware/soft-delete-middleware) Next-generation Node.js and TypeScript ORM
- [Rust](https://docs.rs/diesel-softdelete/latest/diesel_softdelete/) Diesel query builder
- [Python Django](https://github.com/scoursen/django-softdelete) Soft delete for Django ORM, with support for undelete
- [brandur](https://brandur.org/soft-deletion) Soft Deletion Probably Isn't Worth It
- [Evil Martians](https://evilmartians.com/chronicles/soft-deletion-with-postgresql-but-with-logic-on-the-database) Soft deletion with PostgreSQL: but with logic on the database!

## Contribution
This list started as personal collection of interesting things about data versioning. Your contributions and suggestions are warmly welcomed. 
Read the [contribution guidelines](contributing.md).
