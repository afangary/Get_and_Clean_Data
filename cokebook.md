Getting and cleaning data Project Codebook

This file describes the variables, the data, and any transformations or work that you performed to clean up the data
Data source
The site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
The data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Data:
Data was split into 2 main sections Training Data and Test data containing the following files
- 'features_info.txt': Shows information about the variables used on the feature vector.
 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.

The data lists 6 activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)  carried out by 30 Subjects measuring  561 Variables. 
Of those 561 Only 65 Variables of interested indicating mean and standard deviation measurements were selected. 
 
 Variables:
timeBodyAccelerometer-mean()-X       
timeBodyAccelerometer-mean()-Y              
timeBodyAccelerometer-mean()-Z      
timeBodyAccelerometer-std()-X               
timeBodyAccelerometer-std()-Y     
timeBodyAccelerometer-std()-Z               
timeGravityAccelerometer-mean()-X   
timeGravityAccelerometer-mean()-Y           
timeGravityAccelerometer-mean()-Z    
timeGravityAccelerometer-std()-X            
timeGravityAccelerometer-std()-Y     
timeGravityAccelerometer-std()-Z
timeBodyAccelerometerJerk-mean()-X
timeBodyAccelerometerJerk-mean()-Y          
timeBodyAccelerometerJerk-mean()-Z    
timeBodyAccelerometerJerk-std()-X           
timeBodyAccelerometerJerk-std()-Y     
timeBodyAccelerometerJerk-std()-Z           
timeBodygyroscope-mean()-X            
timeBodygyroscope-mean()-Y                  
timeBodygyroscope-mean()-Z            
timeBodygyroscope-std()-X                   
timeBodygyroscope-std()-Y            
timeBodygyroscope-std()-Z                   
timeBodygyroscopeJerk-mean()-X      
timeBodygyroscopeJerk-mean()-Y              
timeBodygyroscopeJerk-mean()-Z      
timeBodygyroscopeJerk-std()-X               
timeBodygyroscopeJerk-std()-Y        
timeBodygyroscopeJerk-std()-Z               
timeBodyAccelerometerMag-mean()      
timeBodyAccelerometerMag-std()              
timeGravityAccelerometerMag-mean()   
timeGravityAccelerometerMag-std()           
timeBodyAccelerometerJerkMag-mean()  
timeBodyAccelerometerJerkMag-std()          
timeBodygyroscopeMag-mean()          
timeBodygyroscopeMag-std()                  
timeBodygyroscopeJerkMag-mean()       
timeBodygyroscopeJerkMag-std()              
frequencyBodyAccelerometer-mean()-X   
frequencyBodyAccelerometer-mean()-Y         
frequencyBodyAccelerometer-mean()-Z   
frequencyBodyAccelerometer-std()-X          
frequencyBodyAccelerometer-std()-Y    
frequencyBodyAccelerometer-std()-Z          
frequencyBodyAccelerometerJerk-mean()-X 
frequencyBodyAccelerometerJerk-mean()-Y     
frequencyBodyAccelerometerJerk-mean()-Z 
frequencyBodyAccelerometerJerk-std()-X      
frequencyBodyAccelerometerJerk-std()-Y  
frequencyBodyAccelerometerJerk-std()-Z      
frequencyBodygyroscope-mean()-X         
frequencyBodygyroscope-mean()-Y             
frequencyBodygyroscope-mean()-Z          
frequencyBodygyroscope-std()-X              
frequencyBodygyroscope-std()-Y          
frequencyBodygyroscope-std()-Z              
frequencyBodyAccelerometerMag-mean()     
frequencyBodyAccelerometerMag-std()         
frequencyBodyBodyAccelerometerJerkMag-mean() 
frequencyBodyBodyAccelerometerJerkMag-std() 
frequencyBodyBodygyroscopeMag-mean()   
frequencyBodyBodygyroscopeMag-std()         
frequencyBodyBodygyroscopeJerkMag-mean() 
frequencyBodyBodygyroscopeJerkMag-std()


Data manipulation steps
The script run_analysis.R manipulates the data in 4 main steps
1.	Merges the training and the test sets to create one data set.
Read the data and bind the train and test data sets using rbind function.

2.	Extracts only the measurements on the mean and standard deviation for each   measurement. 
Find columns with mean and std and extract columns of the data set using select function

3.	Uses descriptive activity names to name the activities in the data set
Using the gsub function to properly name activities

4.	Appropriately labels the data set with descriptive variable names. 
Using the gsub function to properly name activities

5.	From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Using data set created from above steps, create a new tidy Dataset with properly named columns and get the average of each variable. The data is summarized by Subject and Activity. 


