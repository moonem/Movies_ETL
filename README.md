# Movies_ETL

Create a function to perform the **ETL** process on datasets and saving the data on to a **SQL database**.

## Goal of the Analysis

This project is to create one function that takes in the three movie information files gathered from three different sources — **Wikipedia data, Kaggle metadata, and the MovieLens rating data** — and to perform the **Extract-Transform-Load (ETL)** process by adding the data to a **PostgreSQL database**.

## Steps of Analysis

The whole ETL process for three different datasets is a mammoth task. That's why, the overall process is divided into followin four steps:

- **Step 1**: Write an ETL Function to Read Three Data Files
- **Step 2**: Extract and Transform the Wikipedia Data
- **Step 3**: Extract and Transform the Kaggle data
- **Step 4**: Create the Movie Database

### Step 1: Write an ETL Function to Read Three Data Files

The ETL analysis is performed usin Jupyter Notebook. After importing all necessary dependencies, a function named **extract_transform_load** has been created, as shown below, which takes in three arguments; *Wikipedia data, Kaggle metadata, and MovieLens rating data* (from Kaggle).

![extract_transform_load function](https://user-images.githubusercontent.com/58155187/127624208-61fd5751-ae0c-430d-b9eb-5a5ddc7b13aa.png)


### Step 2: Extract and Transform the Wikipedia Data

In this step, a new function **clean_movie(movie)** has been created to initial cleaning up the movie data and keep the column names consistent.

![image](https://user-images.githubusercontent.com/58155187/127625919-66a85e8a-52c9-4f06-bb67-6e60ee7c1b9d.png)

The function **extract_transform_load** created in previous step has been refactored to incorporate **more cleaning** process such as, removing "TV Show" data appeared under movie data, as shown below,

### Step 3: Extract and Transform the Kaggle data

The purpose in this step is similar to the previous Step 2, but the data source is from *Kaggle* which needed the following function **fill_missing_kaggle_data** to be added inside the **extract_transform_load** function block.

![image](https://user-images.githubusercontent.com/58155187/127629614-0c647814-e356-4fda-bc24-86188230dd95.png)


![image](https://user-images.githubusercontent.com/58155187/127626986-09943848-44bb-462e-9ded-67b055dbe54d.png)


Code using **Lambda function** and regular expression **(RegEx)** for parsing monitary "$" figures under *box_office* - is shown in the figure below,

![image](https://user-images.githubusercontent.com/58155187/127628089-36142f20-4dc1-4920-a4b7-644b857d862c.png)


This step also cleaned multiple columns with messy data. Following figure shows how **box_office, budget, release_date, running_time** columns' data has been cleaned,

![image](https://user-images.githubusercontent.com/58155187/127628865-e6baf92c-25ff-46d3-9de1-558c23639049.png)

### Step 4: Create the Movie Database

This step has all the codes from the previous steps and a few more lines of code to **create a PostgreSQL database from Pandas DataFrame** and **read a dataset from the database**. The following figure shows the code-chunk to connect to the created database in local host machine.

![image](https://user-images.githubusercontent.com/58155187/127630662-1b61d0d9-8e52-4b4a-995f-d22ebaa63abf.png)

### Result

Following figures show a gimpse of the three final cleaned DataFrames,

![image](https://user-images.githubusercontent.com/58155187/127632145-800bbf32-60e0-42e0-a2bb-737e92945e94.png)

![image](https://user-images.githubusercontent.com/58155187/127632395-f4c53b15-2c4e-4f79-98a6-049e2190e123.png)




  #### Contact:
  
  **moonem** 
  [m.a.moonem@gmail.com]
