# Hospital Data Analysis Project

## Description

This project involves creating a star schema database for hospital data analysis, generating sample data, performing ETL (Extract, Transform, Load) processes, and setting up foreign key constraints. The star schema consists of dimension tables and a fact table, designed to facilitate efficient querying and reporting.

## Database Schema

The database schema includes the following tables:

1. **DimPatientID**: Contains patient information.
2. **DimTimeID**: Contains date-related information.
3. **DimDoctorID**: Contains doctor information.
4. **Fact_table**: Contains data linking patients, doctors, and dates, along with medical charges.

### Schema Diagram

![Schema Diagram]("C:\Users\LOQ\Pictures\Creating star schema.png")

## Table Definitions

The tables are structured as follows:

- **DimPatientID**: Stores patient details like first name, last name, gender, and age.
- **DimTimeID**: Stores time-related details including day, month, and year.
- **DimDoctorID**: Stores doctor details including name, department, and cost per hour.
- **Fact_table**: Links the dimension tables and stores counts and charges related to medical services.

![Table Definitions]("C:\Users\LOQ\Pictures\Final connections.png")

## Generating Sample Data

We generate sample data for each table and save it in CSV files. This data will be used for analysis and testing the ETL process.

### Sample Data Generation

Sample data is generated for:
- **Patients**: 100 rows of patient details.
- **Time**: 100 rows of date details.
- **Doctors**: 100 rows of doctor details.
- **Facts**: 100 rows linking patients, doctors, and time with medical charges.

![Data Generation]("C:\Users\LOQ\Pictures\row data.png")

## ETL Process

The ETL process involves:

1. **Extract**: Reading data from CSV files.
2. **Transform**: Sorting, merging, and cleansing the data as needed.
3. **Load**: Inserting the data into the SQL Server database tables.

### ETL Steps

![ETL Process]("C:\Users\LOQ\Pictures\Data_loading and table creations.png")
![ETL Process]("C:\Users\LOQ\Pictures\SQL_task_for deleting duplicates.png")

## Setting Foreign Keys

To ensure data integrity, foreign key constraints are set between the fact table and the dimension tables:

- The `PatientId` in the fact table references the `PatientId` in the DimPatientID table.
- The `TimeId` in the fact table references the `TimeId` in the DimTimeID table.
- The `DoctorId` in the fact table references the `DoctorId` in the DimDoctorID table.

![Foreign Keys]("C:\Users\LOQ\Pictures\Connectiong tables together.png")

## Usage

Once the data is loaded and constraints are set, you can run queries to analyze the data. For example, you can query to get doctor names and patient details for a specific year.

### Example Query

An example query might include selecting data based on specific criteria, such as retrieving doctor names and patient details for services rendered in a specific year.


Patients: 100 rows of patient details.
Time: 100 rows of date details.
Doctors: 100 rows of doctor details.
Facts: 100 rows linking patients, doctors, and time with medical charges.

ETL Process
The ETL process involves:

Extract: Reading data from CSV files.
Transform: Sorting, merging, and cleansing the data as needed.
Load: Inserting the data into the SQL Server database tables.
ETL Steps

Setting Foreign Keys
To ensure data integrity, foreign key constraints are set between the fact table and the dimension tables:

The PatientId in the fact table references the PatientId in the DimPatientID table.
The TimeId in the fact table references the TimeId in the DimTimeID table.
The DoctorId in the fact table references the DoctorId in the DimDoctorID table.

Usage
Once the data is loaded and constraints are set, you can run queries to analyze the data. For example, you can query to get doctor names and patient details for a specific year.

Example Query
An example query might include selecting data based on specific criteria, such as retrieving doctor names and patient details for services rendered in a specific year.
