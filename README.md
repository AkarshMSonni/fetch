# fetch
Take home coding test for Fetch Rewards

#Question 1 - Review Existing Unstructured Data and Diagram a New Structured Relational Data Model

Refer to Fetch_Data_Analysis.ipynb for the data wrangling and conversion of JSON files to readable dataframes
ER Diagram can be found in the repo with the name Fetch_ERDiagram.jpeg

JSON files have been normalized to attain a tabular format, columns with nested information are exploded to separate columns and merged into the original dataframes. Additionally, the JSONs have been saved in spearate lines for each record, so the file is being read line-by-line and then appended to a dataframe.

For the data model, the Brands table has been split in to Brands, Category and CPG to attain a normal form. Data from the receipts table has been split into Items and Receipts -> the Item specific information such as barcode, item name, description, brandCode, etc has been moved to the Items table such that each item (and barcode) will be unique per record. Barcode is being used as a primary key in the Items table such that one-to-many relationships can be made with Brands and Receipts table using the barcode field. 

#Question 2 - Write a query that directly answers a predetermined question from a business stakeholder

SQLite3 engine has been used to load the tables in memory, the queries have been written in SQLite dialect, and can be found in the Fetch_Data_Analysis.ipynb notebook under the Q2 section of the notebook



#Question 3 - Evaluate Data Quality Issues in the Data Provided

Evaluation, code and the findings can be found in the Fetch_Data_Analysis.ipynb notebook under the Q3 section


#Question 4 - Communicate with Stakeholders

Email can be found at Fetch_Stakeholder_Email.pdf
