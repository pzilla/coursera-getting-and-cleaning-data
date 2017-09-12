# Coursera "Getting and Cleaning Data" course project

This repository is for the Coursera course "Getting and Cleaning Data" project.
The repository contains the following files:

*  `run_analysis.R`: the R code used to download, clean, transform, create a tidy dataset 
*  `tidy_data.txt`: the output tidy dataset as required by the assignment
*  `CodeBook.md`: a code book that describes the variables, the data, and any transformations/work performed to clean up the data
*  `README.md`: this README file

The `run_analysis.R` script performs the following steps

1. Downloads the dataset into current working directory, and names it `project_dataset.zip`
2. Loads the activity and feature sets
3. Transforms the `feature` set to only include columns with "mean()" or "std()" in column name
4. Loads all the training and test datasets, and only includes columns from the filtered Features set
5. Merges the Traning tables together (`training_set`, `training_labels`, `training_subject`)
6. Merges the Test tables together (`test_set`, `test_labels`, `test_subject`)
7. Combines both Training and Test tables (from preview 2 steps) into one table called `result_data`
8. Update the column names on `result_data` to be meaningful names from downloaded `features` data
9. Update the activity column to be meaningful values from the downloaded `activity_labels` data
10. Summarize `result_data` into a new data.table called `result_data.means` which, which contains the average(mean) of each column, grouped by "subject" and "activity"

The final result is stored in the file `tidy_data.txt`.
