## Getting and Cleaning Data - peer assessment project


## The original data was transformed by

1. Merging the training and the test sets to create one data set.
2. Extracting only the measurements on the mean and standard deviation for each measurement. 
3. Using descriptive activity names to name the activities in the data set
4. Appropriately labeling the data set with descriptive activity names. 
5. Creating a second, independent tidy data set with the average of each variable for each activity and each subject. 



The script takes advantage of the fact that both the test and train directories are structured and named similarly. 
The r_Data function takes a directory name and returns a dataset that is already cleaned and merged with subjects and features.

The mergeDataSet actually generates the two datasets (test and train) and then merges them. It also corrects the Mean and Std names.
The activity_labels then applies the activity labels. The tidy_datafile (which calls tidaydata) then writes it to a file. All these functions are daisy chained. 

* This script relies on the package reshape2
* This script assumes you are running it from the same directory as the dataset i.e. you did a setwd() prior to running it. 