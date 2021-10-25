# Human-Activity-Recognition

The project is part of Coursera Data Science Specialization. 

Run script run_analysis.R from your machine. The script performs tasks which described below. 
CodeBook.md contains detailed description of data set and transformations.

Summary desciption of the script:

Step 1. Script downloads source dataset from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Source dataset contains measurements of variables listed below obtained from 30 volunteers performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. 

Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
Triaxial Angular velocity from the gyroscope.
A 561-feature vector with time and frequency domain variables.
Its activity label.
An identifier of the subject who carried out the experiment.

Detailed characterization of the source dataset can be found in ./dataset/UCI HAR Dataset/README.txt after running run_analysis.R script.

Step 2. Script unzips downloaded data to work directory

Steps 3-5. Script Merges the training and the test sets to create one data set

Step 6. Extracts only the measurements on the mean and standard deviation for each measurement.

Step 7. Uses descriptive activity names to name the activities in the data set

Step 8. Appropriately labels the data set with descriptive variable names (dataset1).

Step 9. From the dataset1, creates a second, independent tidy data set with the average of each variable for each activity and each subject (dataset2)

Step 10. Saves result as dataset1.csv and dataset2.csv to /dataset/UCI HAR Dataset/results
