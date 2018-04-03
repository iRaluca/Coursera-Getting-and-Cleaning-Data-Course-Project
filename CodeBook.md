## Coursera - [Getting and Cleaning Data](https://www.coursera.org/learn/data-cleaning) - Course Project
(Code book)

### Overview - variables - firsttidydataset.csv
* activity
    - list of activities performed by a subject
    - values: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
* subject
     - The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. This variable contains the volunteer number
     - values: 1, 2, 3,...30
* features
     - The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tacc-xyz and tgyro-xyz.      - These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tbodyacc-xyz and tgravityacc-xyz) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.
     - Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tbodyaccjerk-xyz and tbodygyrojerk-xyz). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tbodyaccmag, tgravityaccmag, tbodyaccjerkmag, tbodygyromag, tbodygyrojerkmag).
     - Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fbodyacc-xyz, fbodyaccjerk-xyz, fbodygyro-xyz, fbodyaccjerkmag, fbodygyromag, fbodygyrojerkmag. (Note the 'f' to indicate frequency domain signals). 
     - These signals were used to estimate variables of the feature vector for each pattern: '-xyz' is used to denote 3-axial signals in the X, Y and Z directions.
        - tbodyacc-xyz
        - tgravityacc-xyz
        - tbodyaccjerk-xyz
        - tbodygyro-xyz
        - tbodygyrojerk-xyz
        - tbodyaccmag
        - tgravityaccmag
        - tbodyaccjerkmag
        - tbodygyromag
        - tbodygyroJerkMag
        - fbodyacc-xyz
        - fbodyaccJerk-xyz
        - fbodygyro-xyz
        - fbodyaccmag
        - fbodyaccjerkmag
        - fbodygyromag
        - fbodygyrojerkmag
     - The set of variables that were estimated from these signals are: 
        - mean: Mean value
        - std: Standard deviation

### Overview - variables - secondtidydataset.csv or tidy.txt (contain the same data)
* activity
    - list of activities performed by a subject
    - values: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
* subject
    - The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. This variable contains the volunteer number
    - values: 1, 2, 3,...30
* features
    - all the features variable names described at "firsttidydataset.csv"
    - values:  
        - the average of each variable for each activity and each subject

#### Notes: 
* feature variables are normalized and bounded within [-1,1].  
* The units used for the accelerations (total and body) are 'g's (gravity of earth -> 9.80665 m/seg2).
* The gyroscope units are rad/seg. 

More information can be found [here](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).


### The steps performed by run_analysis() in order to obtain the result of the analysis:
* Downloads the zip file and unzip it to the working directory
* Reads the data files
    - /UCI HAR Dataset/train/X_train.txt
    - /UCI HAR Dataset/train/y_train.txt
    - /UCI HAR Dataset/train/subject_train.txt
    - /UCI HAR Dataset/test/X_test.txt
    - /UCI HAR Dataset/test/y_test.txt
    - /UCI HAR Dataset/test/subject_test.txt
    - /UCI HAR Dataset/activity_labels.txt
    - /UCI HAR Dataset/features.txt
* Merges the training and the test sets to create one data set
* Extracts only the measurements on the mean and standard deviation for each measurement.
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive variable names.
* Generates the first tidy data set (be aware that is a big file)
* From the data set in the previous step, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
* Generates the second tidy data set (aggregated data set using mean function)

### Important notes:
    * System information:
        - Operating system: Windows
        - Platform: x86_64-w64-mingw32
    * R version:
        - 3.3.2 (2016-10-31)
    * Required libraries: 
        - dplyr
        - tidyr