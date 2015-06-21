# Get_and_Clean_Data
coursera Getting and cleaning data project

Introduction
This repo contains project files for Getting and cleaning data Project using R.
There is only one script run_analysis.R
Data obtained from the following URL https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Script:
The script handles the required task in 4 steps
1.	Merges the training and the test sets to create one data set.
2.	Extracts only the measurements on the mean and standard deviation for each measurement. 
3.	Uses descriptive activity names to name the activities in the data set
4.	Appropriately labels the data set with descriptive variable names. 
5.	From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Run the Script:
To run the script ensure the zipped downloadable file is unzipped to WD directly ignoring the root folder UCI HAR Dataset. So content of Train and test data and the features and labels files are directly in the Wording directory  

Final output
The final output of the script is to generate text file “uci_har_meanstd_avg.txt”
