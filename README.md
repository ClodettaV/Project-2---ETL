# Project-2 - ETL

**Purpose and Motivation**

The aim of this project is to assist data analysts in accessing data regarding the 
job market for data science from 2019 to 2021. This will enable data analysts to 
analyse the job requirements and prospects in several areas in Australia. The 
data were sourced from seek.com, one of the leading recruitment platforms in 
Australia. The raw data have been transformed and normalised into meaningful 
set of tables using Pandas on Jupyter notebook and loaded into PostgreSQL 
database.

This code repository contains the solution to perform the ETL on a scheduled 
basis and stores the data in a PostgreSQL Database.

Unit tests have been performed to assure transformation and normalisation has been properly executed.

# Repo structure

```
data/                                       # the tables exported from Jupyter notebooks
docs/                                       # the ERD code, the data definition language (DDL), counts of some of the tables
images/                                     # the ERD diagram
Resources/				    # Raw data
scripts/    
    |__ schema.sql                          # SQL code used to create the target tables 
    |__ Job_role			    # the Jupiter notebook with data transformations on raw data 
    |__ Programming languages tables.ipynb  # the Jupiter notebook with data transformations on raw data
    |__ State and work_type tables.ipynb    # the Jupiter notebook with data transformations on raw data    
    |__ test_etl_function.py                # pytest unit tests 
    |__ etl_function.py              	    # custom user-generated transformation functions 
README.md                                   # all you need to know is in here 

```

**ERD and Data Dictionary**

Entity Relationship Diagram
The ERD diagram was created using: https://app.quickdatabasediagrams.com/#/

![image](https://user-images.githubusercontent.com/88511756/145743861-4ed8e059-e5b4-40b9-920a-9e279ebe3db5.png)

**Data dictionary**

Below are the data definitions for the following tables:

<b>`Job Title`</b>
|Column name| Definition |
|-|-|
|jobId|The unique ID for the job|
|jobTitle|The title of each job|
|jobRole|Broader job title

<b>`Programming languages`</b> 
|Column name| Definition|
|-|-|
|jobId|The unique ID for the job|
|R|Programming language either required (1) or not(0) for each job|
|Matlab|Programming language either required (1) or not(0) for each job|
|Python|Programming language either required (1) or not(0) for each job|
|Kavascript|Programming language either required (1) or not(0) for each job|
|SQL|Programming language either required (1) or not(0) for each job|
|Tableau|Programming language either required (1) or not(0) for each job|
|C|Programming language either required (1) or not(0) for each job|
|Java|Programming language either required (1) or not(0) for each job|
|Ruby|Programming language either required (1) or not(0) for each job|

<b>`State`</b>  
|Column name| Definition|
|-|-|
|jobId|The unique ID for the job|
|state|The state where the job is based |

<b>`Work Type`</b>  
|Column name| Definition|
|-|-|
|jobId|The unique ID for the job|
|Industry|The renamed job classification|
|Departments|The renamed job sub-classification|
|Works_type|The type of contract|


Usage
The required python libraries and version are 

	
## Python dependencies 

- pandas==1.3.2
- sqlalchemy==1.4.26
- pytest==6.2.5

Install python dependencies by performing:

```
pip install -r 
```

## Running code locally 
To run the ETL code on your computer, execute the following in your terminal: 

```
cd scripts
python -m jupyter nbconvert --to python scripts
python scripts/etl_functions.py
```

## Run unit tests 
To run the unit tests on your computer, execute the following in your terminal: 

```
pytest scripts
```

You should see the following output: 

```
========================================================================== warnings summary =========================================================================== 
..\..\anaconda3\lib\site-packages\pyreadline\py3k_compat.py:8
  C:\Users\Laurent\anaconda3\lib\site-packages\pyreadline\py3k_compat.py:8: DeprecationWarning: Using or importing the ABCs from 'collections' instead of from 'collections.abc' is deprecated since Python 3.3, and in 3.9 it will stop working
    return isinstance(x, collections.Callable)

-- Docs: https://docs.pytest.org/en/stable/warnings.html
==================================================================== 1 passed, 1 warning in 0.55s ===================================================================== 
```

## Scheduling jobs 


<details>
<summary><strong> Cron (MacOS or Linux) </strong></summary>
'''
'''
</details>

# Contributors
- [@ClodettaV](https://github.com/ClodettaV)
- [@Lau](https://github.com/Lau)
- [@MonikaSidhu1](https://github.com/MonikaSidhu1)

