# data-analysis

All things on data wrangling methods and data analysis using python & R

## ETL (Extract, Transform, Load)
1. Extract
   - From various sources (APIs, Databases-MySQL/PostgreSQL, Flat files)
2. Transform
   - Remove duplicates, NA/Null values, outliers etc.
   - Normalise/Standardise values (eg. dates, z-score calc)
   - Merge datasets, convert data types
3. Load
   - Store transformed data into a data warehouse(eg. Redshift)/lake
   - Data warehouses store multiple kinds of data (for diff purposes - summary, mining, metadata) from many heterogenous data sources


## Brief note on data modelling & PowerBI
1. Extract data (Home > Get Data)
2. Data cleaning with Power Query Editor (Transform data > Power Query Editor)
3. Data modelling (switch to model view)
   - Set r/s between tables, Define cardinality (many-to-one, one-to-many), DAX (Data Analysis Expressions) columns & measures
   - DAX columns (eg. Profit = Sales[Revenue] - Sales[Costs])
   - DAX measures (eg. Profit = SUM(Sales[Revenue]) - SUM(Sales[Costs]) => Measures are more efficient than columns
4. IF() vs SWITCH
   - Status = IF(Sales[Revenue] > 10000, "High", "Low")
   - Category = 
      SWITCH(
          TRUE(),
          Sales[Revenue] > 10000, "High",
          Sales[Revenue] > 5000, "Medium",
          Sales[Revenue] > 0, "Low",
          "No Sales"
      )



