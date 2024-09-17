# Crowdfunding ETL Mini Project

## Project Overview
This project focuses on building an ETL (Extract, Transform, Load) pipeline using Python, Pandas, and either Python dictionary methods or regular expressions. The goal is to extract data from multiple sources, transform it into usable formats, and load the data into a PostgreSQL database. The project involves creating four CSV files from the transformed data, designing an ERD, and implementing a database schema in Postgres.

### Project Objectives:
1. Extract and transform data from Excel files.
2. Create and export CSV files containing transformed data.
3. Design and implement a relational database schema.
4. Load the CSV data into a PostgreSQL database.
5. Verify database integrity by querying the data.

## Files and Resources
Download the starter files and code for the project from [Project 2 ETL Files](#).

**Resources Provided:**
- `ETL_Mini_Project_starter_code.ipynb`
- `crowdfunding.xlsx`
- `contacts.xlsx`

## Instructions

### Repository Setup:
1. Create a new repository called **Crowdfunding_ETL** and add your partner as a collaborator.
2. Clone the repository to your local machine.
3. Rename the `ETL_Mini_Project_starter_code.ipynb` file to include both team members' initials (e.g., `ETL_Mini_Project_JDoe_ASmith.ipynb`).
4. Add the `Resources` folder containing the provided Excel files to your repository and push changes to GitHub.
5. Ensure that both team members pull the changes to their local machines.

### Steps:

#### 1. Create the Category and Subcategory DataFrames
- Extract and transform data from `crowdfunding.xlsx` to create two DataFrames:
  - **Category DataFrame**: 
    - Columns: `category_id` (sequential), `category` (category titles)
  - **Subcategory DataFrame**: 
    - Columns: `subcategory_id` (sequential), `subcategory` (subcategory titles)
- Export these DataFrames as `category.csv` and `subcategory.csv`.

#### 2. Create the Campaign DataFrame
- Extract and transform data from `crowdfunding.xlsx` to create the **Campaign DataFrame**:
  - Columns: `cf_id`, `contact_id`, `company_name`, `description`, `goal`, `pledged`, `outcome`, `backers_count`, `country`, `currency`, `launch_date`, `end_date`, `category_id`, `subcategory_id`.
- Convert columns to the appropriate data types (e.g., float, datetime).
- Export this DataFrame as `campaign.csv`.

#### 3. Create the Contacts DataFrame
- Choose between two methods for transforming the `contacts.xlsx` data:
  - **Option 1**: Use Python dictionary methods to extract and clean the data.
  - **Option 2**: Use regular expressions to extract the contact details.
- Split the `name` column into `first_name` and `last_name`.
- Export the cleaned DataFrame as `contacts.csv`.

#### 4. Create the Crowdfunding Database
- Sketch an ERD (Entity Relationship Diagram) using QuickDBD to visualize the relationships between tables.
- Design and implement the database schema in PostgreSQL. Save the schema as `crowdfunding_db_schema.sql`.
- Create the database `crowdfunding_db` and define tables according to the schema.
- Import the CSV data into the corresponding tables.
- Verify the import by running `SELECT` queries on each table.

## Deliverables

### CSV Files
- `category.csv`
- `subcategory.csv`
- `campaign.csv`
- `contacts.csv`

### Database Schema and ERD
- `crowdfunding_db_schema.sql`
- ERD sketch

### PostgreSQL Database
- `crowdfunding_db`

### Queries:
- Use `SELECT * FROM <table_name>` to verify that each table contains the correct data.
