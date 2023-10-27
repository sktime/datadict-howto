# datadict-howto

## What is a data dictionary?

A data dictionary is a "manual" accompanying a data source or data set.

Its main purpose is to provide the reader information about:

* information on points of contact in relation to the data, e.g., data stewards, data owners
* information on the content of the data, most importantly:
    * provenance of the data: how obtained, how sampled, collection purpose
    * interface concerns, if a data source, e.g., use of APIs
    * optimally, full technical specifications of files, formats, interfaces, etc
* further information relevant to use of the data, e.g., "getting started" tutorials, legal considerations (licenses)

## Example data dictionaries

Data dictionaries can be written in formulaic ways. Typical sections:

* header with versions and register of changes
* a summary of data steward, owner, usage
* a high-level description of the content
* a detail description of the tables (or interfaces)

Data version management tools such as dvc facilitate programmatic updates
and curation of data registers.

An example follows.

# Data Dictionary - Pet Register

## Dictionary Version and Change Log

- **Last Version**: 1.1
- **Last Updated**: November 15, 2023
- **Change Log**:

| Date       | Version | Description                 | Author        |
|------------|---------|-----------------------------|---------------|
| 2023-11-15 | doc1.1  | Updated table descriptions  | Gabor Göre    |
| 2023-10-27 | doc1.0  | Initial dictionary created  | Matthew Ludas |

## Data Version and Change Log

- **Last Version**: 1.2
- **Last Updated**: October 31, 2023
- **Change Log**:

| Date       | Version | Description                      | Author        |
|------------|---------|----------------------------------|---------------|
| 2023-10-31 | 1.2     | Removed erroneous duplications   | Matthew Ludas |
| 2023-10-28 | 1.1     | Fixed erroneous NA values        | Matthew Ludas |
| 2023-10-27 | 1.0     | Initial version created          | Matthew Ludas |

## Data Steward and Owner

- **Data Steward**: Franz Xaver Eder
- **Data Owner**: ELTE Animal Shelter

## High-Level Description

The pet register database contains information about cats and dogs at the ELTE Animal Shelter.
It includes data on each pet's name, type, and weight.

This dataset was exported from the pet register database for research purposes
by Matthew Ludas on 2023-10-27, to develop
a machine learning model to distinguish cats from dogs.

## Tables

The dataset consists of a single table, `pets.csv`, stored in the
repository

### Table: `pets.csv`

- **Description**: This table stores information about cats and dogs at the ELTE Animal Shelter.
- **Rows** (total: 252) correspond to individual pets, registered at the ELTE Animal Shelter on 2023-10-27.
- **Columns** (total: 4) correspond to different observables of the individual pets:
- **ID columns** (total: 1) are: PetID

Columns:
| Column Name | Abstract type | Data Type    | Description                   |
|-------------|---------------|--------------|-------------------------------|
| PetID       | integer       | INT          | Unique identifier for the pet |
| Name        | string        | VARCHAR(50)  | Name of the pet               |
| Type        | categorical   | VARCHAR(10)  | Type of pet (Cat or Dog)      |
| Weight      | float         | DOUBLE       | Weight of the pet in kg       |


#### sample (first five rows)

| PetID | Name      | Type  | Weight |
|-------|-----------|-------|--------|
| 1     | Fluffy    | Cat   | 4.5    |
| 2     | Max       | Dog   | 12.2   |
| 3     | Whiskers  | Cat   | 5.1    |
| 4     | Buddy     | Dog   | 8.7    |
| 5     | Luna      | Cat   | 3.4    |
