# **Project 2: Data Processing and Dimensionality Reduction**

## **Overview**

This notebook processes and analyzes player and match event data, integrating multiple data sources to extract useful insights. The analysis includes data loading, preprocessing, and dimensionality reduction using PCA. The goal is to rank the attacking players based off PCA.

## **Requirements**

This notebook was run on Python version 3.9.6. The following Python libraries are required:

* pandas  
* numpy  
* matplotlib  
* seaborn  
* scikit-learn  
* rds2py (for reading .rds files)

## **Data Sources**

The notebook loads the following datasets:

* `atlutd_datascientist_project2_player_mins_appearances.csv`: Contains player minutes and appearances.  
* `atlutd_datascientist_project2_schedule.csv`: Provides match schedule details.  
* `atlutd_datascientist_project2_eventdata.rds`: Stores match event data in RDS format.

## **Steps Included**

1. **Data Loading and Cleaning**

   * Reading `.csv` and `.rds` files  
   * Converting `.rds` data to a Pandas DataFrames per what's needed for the analysis that follows (assist info is in one dataframe, while other events are stored in another)  
2. **Data Preprocessing**

   * Filtering out non-attacking players and players that are not getting a lot of minutes  
   * Extracting desired metrics  
   * Standardizing numerical features  
3. **Ranking**

   * Applying Principal Component Analysis (PCA) to reduce feature dimensionality  
   * Ranking the players based off the principal components and determining which metrics the PCs correlate to

## **How to Use**

1. Ensure all dependencies are installed.  
2. Place the required datasets in the appropriate directory.  
3. Run the notebook sequentially to preprocess and analyze the data.

## **Output**

A cleaned dataset with reduced dimensions, ready for further modeling and analysis. There are tables with the top three players that contain their id number and the metrics (goals scored, cards total, etc) as well as plots of the players on the principal components.

