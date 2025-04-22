# Big Data System

This project outlines a big data system for mobility-on-demand car location data.

## Architecture Diagram

# ciel_big_data_system
graph LR
    A[User] --> B{Plan Big Data System};
    B --> C[Mobility on Demand Car Location Data];
    C --> I[InfluxDB];
    I --> D[MongoDB];
    B --> E[Periodically];
    B --> F[Backup to HDFS];
    F --> G[Telegraf and HDFS];
    B --> H[Apache Hadoop];
    B --> J[Backup PostgreSQL to HDFS];
    J --> G;
    J --> L[PostgreSQL Input Plugin];
    L --> M[PostgreSQL];
    D --> G;
    G --> K[HDFS];
