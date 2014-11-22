# CodeBook

The CodeBook describes the variables, data, any transformations or work that has been done 
to clean the data.

# Objectives

The objectives of the script 'run_analysis.R' can be described in the following five points -

* 1. Merges the training and the test sets to create one data set. 
All the data having the same number of columns and that referred to same object or entity were merged using 'rbind()' function

* 2. Extracts only the measurements on the mean and standard deviation for each measurement. 
The columns with the standard deviation and mean were extracted from the dataset and the columns
were given proper names as described in the 'features.txt' document. 

* 3. Uses descriptive activity names to name the activities in the data set. 
The activity names and IDs were taken from the 'activity_labels.txt' document and were properly substituted in the dataset.

* 4. Appropriately labels the data set with descriptive activity names.
The column names were corrected properly.

* 5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
A new dataset was created with all the mean measurements for each subject and activity. 
The output file was named 'result.txt'.



# Variable Names and their meaning

* The variables were named according to the downloaded file names as follows:  'x_train', 'y_train', 'x_test', 'y_test', 'subject_train' and 'subject_test'

* The above mentioned datasets were merged to produce 'x_data', 'y_data' and 'subject_data'

* Proper names were applied to the 'x_data' dataset which were extracted from the 'features' document
and were saved into 'mean_sd' vector

* Same was done for the 'activities'.

* The 'x_data', 'y_data' and 'subject_data' were merged into a giant dataset named 'all_data'

* Using the ddply() function from the plyr package, the colMeans() were calculated and saved into the
'result' variable which was eventually saved as a text file.
