# khosyi_adf

This azure data factory pipeline project works as follow:
--
Sample excel files in Azure data lake  >--LOAD--> Azure SQL DB  >--TRANSFORM--> Azure SQL DB and Synapse Serverless SQL

Sample excel files in azure data lake:
- payroll 2020
- payroll 2021
- agency dimension table
- employee dimension table
- title dimension table

The above sample files are loaded into Azure SQL DB and then transformed by using union, filter with parameterisation, derived columns,
and aggregation to create a fact table for total pay given to the different agencies in the selected year. This aggregated summary table is then
loaded back into the azure sql db as a summary table and also into the serverless sql external table in azure synapse.
