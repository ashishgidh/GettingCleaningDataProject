# Introduction

The script `run_analysis.R` executed the steps as required by the project in the course. 

The training and test data sets are first loaded into variables and then are first merged together using the rbind function. 
Using the features dataset only the mean and standard deviation measurements are taken. The grep function was used to search for a specific values of min() or std()
The column names are also cleaned with the features columns to make them mode readable. 
The activity data is updated using the values from the `activity_labels.txt` file.
Finally, using the ddply function the avaerages data is calculated group by subject and activity type. The output file is called `averages_data.txt` which is also uploaded. 

# Variables

`x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` has data from the downloaded files.
`x_data`, `y_data` and `subject_data` merge the previous datasets to further analysis.
`features` contains the names for the `x_data` dataset
'meanstd_features`  is a numeric vector used to get the desired data.
The same is done using the desc_activities variable. 
`final_data` merges `x_data`, `y_data` and `subject_data` 
`averages_data` has averages stored in a `.txt` file. `ddply()` was used apply `colMeans()`
