
This code book describes the input data, steps to process the data and the processed output data. 
This project is to tidy raw data for further analysis. The raw data in this project is from experiments for wearable computing.

## Raw data
The raw data and the details of the raw data and variables are available here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## Processing
The steps used to process the raw data in this projects are:
* Read subject and activity details from test and train data files
* Read the test data from test and train data files (X_test.txt, X_train.txt)
* Read feature details from feature.txt
* Combine test and train datasets into a single dataset
* Add subject and activity variables to the combined dataset
* Remove all columns except Subject, Activity and mean and standard deviation columns
* Compute the average of mean and standard deviation columns grouped by Subject and Activity
* Return the resulting dataset as a data frame

## Variables
The resulting tidy data (data frame) has the following variables:
* Subject - Identifier of the subject in the experiment. There are 30 subjects and this variable range is 1 to 30
* Activity - The activity that the data in the row is for. Values are WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING

The remaining variables are processed values of the corresponding raw data variable. 
The original raw dataset has 561 different variables measured from the accelerometer and gyroscope of the phone used by the subject. The raw variables
are mean and standard deviation of 128 readings produced from a 50Hz sampling during a 2.56s periood. The following variables exist in the processed data 
are average values of the corresponding raw data variable.

The complete list of variables in the output data is:

	1.                      Subject
	2.                     Activity
	3.            tBodyAcc-mean()-X
	4.            tBodyAcc-mean()-Y
	5.            tBodyAcc-mean()-Z
	6.             tBodyAcc-std()-X
	7.             tBodyAcc-std()-Y
	8.             tBodyAcc-std()-Z
	9.         tGravityAcc-mean()-X
	10.        tGravityAcc-mean()-Y
	11.        tGravityAcc-mean()-Z
	12.         tGravityAcc-std()-X
	13.         tGravityAcc-std()-Y
	14.         tGravityAcc-std()-Z
	15.       tBodyAccJerk-mean()-X
	16.       tBodyAccJerk-mean()-Y
	17.       tBodyAccJerk-mean()-Z
	18.        tBodyAccJerk-std()-X
	19.        tBodyAccJerk-std()-Y
	20.        tBodyAccJerk-std()-Z
	21.          tBodyGyro-mean()-X
	22.          tBodyGyro-mean()-Y
	23.          tBodyGyro-mean()-Z
	24.           tBodyGyro-std()-X
	25.           tBodyGyro-std()-Y
	26.           tBodyGyro-std()-Z
	27.      tBodyGyroJerk-mean()-X
	28.      tBodyGyroJerk-mean()-Y
	29.      tBodyGyroJerk-mean()-Z
	30.       tBodyGyroJerk-std()-X
	31.       tBodyGyroJerk-std()-Y
	32.       tBodyGyroJerk-std()-Z
	33.          tBodyAccMag-mean()
	34.           tBodyAccMag-std()
	35.       tGravityAccMag-mean()
	36.        tGravityAccMag-std()
	37.      tBodyAccJerkMag-mean()
	38.       tBodyAccJerkMag-std()
	39.         tBodyGyroMag-mean()
	40.          tBodyGyroMag-std()
	41.     tBodyGyroJerkMag-mean()
	42.      tBodyGyroJerkMag-std()
	43.           fBodyAcc-mean()-X
	44.           fBodyAcc-mean()-Y
	45.           fBodyAcc-mean()-Z
	46.            fBodyAcc-std()-X
	47.            fBodyAcc-std()-Y
	48.            fBodyAcc-std()-Z
	49.       fBodyAccJerk-mean()-X
	50.       fBodyAccJerk-mean()-Y
	51.       fBodyAccJerk-mean()-Z
	52.        fBodyAccJerk-std()-X
	53.        fBodyAccJerk-std()-Y
	54.        fBodyAccJerk-std()-Z
	55.          fBodyGyro-mean()-X
	56.          fBodyGyro-mean()-Y
	57.          fBodyGyro-mean()-Z
	58.           fBodyGyro-std()-X
	59.           fBodyGyro-std()-Y
	60.           fBodyGyro-std()-Z
	61.          fBodyAccMag-mean()
	62.           fBodyAccMag-std()
	63.  fBodyBodyAccJerkMag-mean()
	64.   fBodyBodyAccJerkMag-std()
	65.     fBodyBodyGyroMag-mean()
	66.      fBodyBodyGyroMag-std()
	67. fBodyBodyGyroJerkMag-mean()
	68.  fBodyBodyGyroJerkMag-std()
	