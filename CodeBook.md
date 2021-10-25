---
editor_options: 
  markdown: 
    wrap: 72
---

**File contains:**

\- Summary description of project goal and steps

\- Description of result datasets

\- Detailed description of data transformation and code

------------------------------------------------------------------------

Current project has a goal to develop a script run_analysis.R which
performs following:

**Step 1\*.** Script downloads source dataset from
<https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>

Source dataset contains measurements of variables listed below obtained
from 30 volunteers performed six activities (WALKING, WALKING_UPSTAIRS,
WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone
(Samsung Galaxy S II) on the waist. Using its embedded accelerometer and
gyroscope, we captured 3-axial linear acceleration and 3-axial angular
velocity at a constant rate of 50Hz. - Triaxial acceleration from the
accelerometer (total acceleration) and the estimated body acceleration.

-   Triaxial Angular velocity from the gyroscope.

-   A 561-feature vector with time and frequency domain variables.

-   Its activity label.

-   An identifier of the subject who carried out the experiment.

Detailed characterization of the source dataset can be found in
./dataset/UCI HAR Dataset/README.txt after running run_analysis.R
script.

**Step 2.** Script unzips downloaded data to work directory

**Steps 3-5.** Script Merges the training and the test sets to create
one data set

**Step 6.** Extracts only the measurements on the mean and standard
deviation for each measurement.

**Step 7.** Uses descriptive activity names to name the activities in
the data set

**Step 8.** Appropriately labels the data set with descriptive variable
names (dataset1).

**Step 9.** From the dataset1, creates a second, independent tidy data
set with the average of each variable for each activity and each subject
(dataset2)

**Step 10.** Saves result as dataset1.csv and dataset2.csv to
/dataset/UCI HAR Dataset/results

+:----------------------------------------------------------------------+
| \* - Details of each step and code are given after result datasets    |
| description                                                           |
+-----------------------------------------------------------------------+

**Result "dataset1"**

Data set contains vectors of 44 measured variables for each activity and
subject obtained from source dataset files located in following folders:

dataset\\UCI HAR Dataset\\test\
dataset\\UCI HAR Dataset\\train

Only time domain variables are extracted. Source data set variable names
can be produced from source data set variables subset mentioned below by
removing -XYZ suffix and adding suffixes -mean(), -std(), -X, -Y, -Z.
See detailed code below for more details.

**dataset1 contains following variables:**

[1] "activity_id" - id of activity obtained from activity_labels.txt of
source data set\
[2] "activity_description" - description of activity obtained from
activity_labels.txt of source data set\
[3] "subject_id" - subject id obtained from files subject_train.txt and
subject_test.txt

[4-9] Average of mean and standard deviation (stdev) of body triaxial
linear acceleration (tBodyAcc-XYZ variables subset in source data set)\
[4] "body_linear_acceleration_mean_X"\
[5] "body_linear_acceleration_mean_Y"\
[6] "body_linear_acceleration_mean_Z"\
[7] "body_linear_acceleration_stdev_X"\
[8] "body_linear_acceleration_stdev_Y"\
[9] "body_linear_acceleration_stdev_Z"

[10-15] Average of mean and standard deviation (stdev) of gravity
triaxial linear acceleration (tGravityAcc-XYZ variables subset in source
data set)\
[10] "gravity_linear_acceleration_mean_X"\
[11] "gravity_linear_acceleration_mean_Y"\
[12] "gravity_linear_acceleration_mean_Z"\
[13] "gravity_linear_acceleration_stdev_X"\
[14] "gravity_linear_acceleration_stdev_Y"\
[15] "gravity_linear_acceleration_stdev_Z"

[16-21] Average of mean and standard deviation (stdev) of body triaxial
linear acceleration time derivative (tBodyAccJerk-XYZ variables subset
in source data set)\
[16] "body_linear_acceleration_derivative_mean_X"\
[17] "body_linear_acceleration_derivative_mean_Y"\
[18] "body_linear_acceleration_derivative_mean_Z"\
[19] "body_linear_acceleration_derivative_stdev_X"\
[20] "body_linear_acceleration_derivative_stdev_Y"\
[21] "body_linear_acceleration_derivative_stdev_Z"

[22-27] Average of mean and standard deviation (stdev) of body angular
velocity (tBodyGyro-XYZ variables subset in source data set)\
[22] "body_angular_velocity_mean_X"\
[23] "body_angular_velocity_mean_Y"\
[24] "body_angular_velocity_mean_Z"\
[25] "body_angular_velocity_stdev_X"\
[26] "body_angular_velocity_stdev_Y"\
[27] "body_angular_velocity_stdev_Z"

[28-33] Average of mean and standard deviation (stdev) of body angular
velocity time derivative (tBodyGyroJerk-XYZ variables subset in source
data set)\
[28] "body_angular_velocity_derivative_mean_X"\
[29] "body_angular_velocity_derivative_mean_Y"\
[30] "body_angular_velocity_derivative_mean_Z"\
[31] "body_angular_velocity_derivative_stdev_X"\
[32] "body_angular_velocity_derivative_stdev_Y"\
[33] "body_angular_velocity_derivative_stdev_Z"

[34-43] Mean and standard deviation (stdev) of magnitude (calculated
using Euclidean norm) for each variable described above:

tBodyAccMag variables subset in source dataset\
[34] "body_linear_acceleration_magnitude_mean" \
[35] "body_linear_acceleration_magnitude_stdev"

\
tGravityAccMag variables subset in source dataset\
[36] "gravity_linear_acceleration_magnitude_mean" \
[37] "gravity_linear_acceleration_magnitude_stdev"\

tBodyAccJerkMag variables subset in source dataset\
[38] "body_linear_acceleration_derivative_magnitude_mean" \
[39] "body_linear_acceleration_derivative_magnitude_stdev" \

tBodyGyroMag variables subset in source dataset\
[40] "body_angular_velocity_magnitude_mean"\
[41] "body_angular_velocity_magnitude_stdev"\

tBodyGyroJerkMag variables subset in source dataset\
[42] "body_angular_velocity_derivative_magnitude_mean"\
[43] "body_angular_velocity_derivative_magnitude_stdev"

[44] "set_id" - set id: 1 - test data set, 2 - train data set.

**Result "dataset2" contains following variables:**

[1] Unique identifier which consists of activity name and subject id:

[1] "activity_subject_id"

[2-7] Average of mean and standard deviation (stdev) of body triaxial
linear acceleration

[2] "average_body_linear_acceleration_mean_X"\
[3] "average_body_linear_acceleration_mean_Y"\
[4] "average_body_linear_acceleration_mean_Z"

[5] "average_body_linear_acceleration_stdev_X"\
[6] "average_body_linear_acceleration_stdev_Y"\
[7] "average_body_linear_acceleration_stdev_Z"

[8-13] Average of mean and standard deviation (stdev) of gravity
triaxial linear acceleration

[8] "average_gravity_linear_acceleration_mean_X"\
[9] "average_gravity_linear_acceleration_mean_Y"\
[10] "average_gravity_linear_acceleration_mean_Z"\
[11] "average_gravity_linear_acceleration_stdev_X"\
[12] "average_gravity_linear_acceleration_stdev_Y"\
[13] "average_gravity_linear_acceleration_stdev_Z"

[14-19] Average of mean and standard deviation (stdev) of body triaxial
linear acceleration time derivative

[14] "average_body_linear_acceleration_derivative_mean_X"\
[15] "average_body_linear_acceleration_derivative_mean_Y"\
[16] "average_body_linear_acceleration_derivative_mean_Z"\
[17] "average_body_linear_acceleration_derivative_stdev_X"\
[18] "average_body_linear_acceleration_derivative_stdev_Y"\
[19] "average_body_linear_acceleration_derivative_stdev_Z"

[20-25] Average of mean and standard deviation (stdev) of body triaxial
angular velocity

[20] "average_body_angular_velocity_mean_X"\
[21] "average_body_angular_velocity_mean_Y"\
[22] "average_body_angular_velocity_mean_Z"\
[23] "average_body_angular_velocity_stdev_X"\
[24] "average_body_angular_velocity_stdev_Y"\
[25] "average_body_angular_velocity_stdev_Z"

[26-31] Average of mean and standard deviation (stdev) of body triaxial
angular velocity time derivative

[26] "average_body_angular_velocity_derivative_mean_X"\
[27] "average_body_angular_velocity_derivative_mean_Y"\
[28] "average_body_angular_velocity_derivative_mean_Z"\
[29] "average_body_angular_velocity_derivative_stdev_X"\
[30] "average_body_angular_velocity_derivative_stdev_Y"\
[31] "average_body_angular_velocity_derivative_stdev_Z"

[32-41] Average magnitude (calculated using Euclidean norm) for each
variable mentioned above

[32] "average_body_linear_acceleration_magnitude_mean"\
[33] "average_body_linear_acceleration_magnitude_stdev"\
[34] "average_gravity_linear_acceleration_magnitude_mean"\
[35] "average_gravity_linear_acceleration_magnitude_stdev"\
[36] "average_body_linear_acceleration_derivative_magnitude_mean"\
[37] "average_body_linear_acceleration_derivative_magnitude_stdev"\
[38] "average_body_angular_velocity_magnitude_mean"\
[39] "average_body_angular_velocity_magnitude_stdev"\
[40] "average_body_angular_velocity_derivative_magnitude_mean"\
[41] "average_body_angular_velocity_derivative_magnitude_stdev"

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

**Code Book**

Details of data transformation and code are given below.

\#1 Create directory "dataset" and download dataset zip to the directory

`if (!file.exists("dataset")) { dir.create("dataset") } download.file("https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip",destfile = "./dataset/data.zip")`

\#2 sets work directory to dataset, unzip data.zip to the dataset
directory - utils library is required, utils library should be installed

`library(utils) setwd("./dataset") unzip("data.zip")`

\#3 read txt files from the dataset files and prepare for merging

\#3.1 read features (variables) list from features.txt to variables
dataframe

`setwd("./UCI HAR Dataset")`

\#changes wd

`variables<-read.table("./features.txt")`

\#3.2 subset variable names vector from variables

`dataframe variables<-variables$V2`

\#3.3 read activity_labels.txt to activities dataframe and create
descriptive names for variables ("activity_id" and
"activity_description")

`activities<-read.table("./activity_labels.txt") names(activities)<-c("activity_id","activity_description")`

\#3.4 read 'train/X_train.txt' (Training set) to trainingset dataframe
and assign variable names from "variables" vector

`trainingset<-read.table("./train/X_train.txt") names(trainingset)<-variables`

\#3.5 read 'train/y_train.txt' (Training labels) to traininglabels
dataframe and assign "activity_id" name to the variable

`traininglabels<-read.table("./train/y_train.txt") names(traininglabels)<-"activity_id"`

\#3.6 read 'train/subject_train.txt' (subjects) to trainingsubjects
dataframe and assign "subject_id" name to the variable

`trainingsubjects<-read.table("./train/subject_train.txt") names(trainingsubjects)<-"subject_id"`

\#3.7 read 'test/X_test.txt' (testing set) to testingset dataframe and
assign variable names from "variables" vector

`testingset<-read.table("./test/X_test.txt") names(testingset)<-variables`

\#3.8 read 'test/y_test.txt' (testing labels) to testinglabels dataframe
and assign "activity_id" name to the variable

`testinglabels<-read.table("./test/y_test.txt") names(testinglabels)<-"activity_id"`

\#3.9 read 'test/subject_test.txt' (subjects) to testingsubjects
dataframe and assign "subject_id" name to the variable

`testingsubjects<-read.table("./test/subject_test.txt") names(testingsubjects)<-"subject_id"`

\#4 bind labels with datasets

\#4.1 bind testingslabels with testingset to testingset dataframe,
remove testinglabels

`testingset<-cbind(testinglabels,testingset) rm(testinglabels)`

\#4.2 bind testingset with testingsubjects to testingset dataframe,
remove testingsubjects

`testingset<-cbind(testingsubjects,testingset) rm(testingsubjects)`

\#4.3 bind traininglabels with trainingset to trainingset dataframe,
remove traininglabels

`trainingset<-cbind(traininglabels,trainingset) rm(traininglabels)`

\#4.4 bind trainingset with trainingsubjects to trainingset dataframe,
remove trainingsubjects

`trainingset<-cbind(trainingsubjects,trainingset)rm(trainingsubjects)`

\#5 join trainingset and testingset - dplyr and plyr packages are
required add categorization variable "set_id" to identify dataset if
needed

`library(dplyr) library(plyr)`

\#5.1 create dataframe "datasets" which consists of variables "set_id" -
"set_description" \#set_id = 1 for testingset, set_id = 2 for
trainingset

`datasets<-data.frame(set_id=c("1","2"), set_description=c("test","train"))`

\#5.2 create variable "set_id" in testingset and assign value 1

`testingset$set_id<-1`

\#5.3 create variable "set_id" in trainingset and assign value 2

`trainingset$set_id<-2`

\#5.4 bind "testingset" and "trainingset"

`dataset1<-bind_rows(testingset,trainingset)`

\#6 Select only id, mean and stadard deviation variables \#6.1 create
vector "vars" of variable names from "dataset1" which contains "id",
"mean" or "std" literals

`vars<-grep("id|mean()|std()",names(dataset1))`

\#6.2 extract variables which have numbers defined by vector "vars" from
"dataset1" to "dataset2"

`dataset2<-select(dataset1,all_of(vars))`

\#6.3 create vector "vars" of variable names from "dataset2" which
contains "Freq" literal

`vars<-grep("Freq",names(dataset2))`

\#6.4 extract all variables except those which have numbers defined by
vector "vars" from "dataset1" to "dataset3" \#frequency domain variables
don't contain results of measurements, only FFT calculation results

`dataset3<-select(dataset2,-all_of(vars))`

\#6.5 create vector "vars" of variable names from "dataset3" which
starts with "f" (Frequency domain variables)

`vars<-grep("^f",names(dataset3))`

\#6.6 extract all variables except those which have numbers defined by
vector "vars" from "dataset3" to "dataset4"

`dataset4<-select(dataset3,-all_of(vars))`

\#6.7 create vector "vars" of variable names from "dataset4" which
contains "Jerk" literals (time derivatives of measurements) \#time
derivaties measurements, only FFT calculation results

`vars<-grep("^f",names(dataset3))`

\#7 join "dataset5" data frame with from "dataset4" by "activity_Id":
adds "activity_description" variable from "activities" data frame

`dataset5<-join(activities,dataset4,by ="activity_id", type="inner")`

\#8 assign descriptive variable names \#8.1 create vector "vars"
containing names of variables from "dataset5"\
`vars<-names(dataset5)`

\#8.2 remove "t" prefix from elements of "vars"
vars\<-gsub("\^t","",vars)

\#8.3 replace literals in elements of "vars"

"Body" with "body\_" \
"Gravity" with "gravity\_" \
"Acc" with "linear_acceleration\_" \
"Gyro" with "angular_velocity\_" \
"Jerk" with "derivative\_" \
"Mag" with "magnitude\_" \
"-mean" with "mean\_" \
"-std" with "stdev\_"

`vars<-gsub("Body","body_",vars)`

`vars<-gsub("Gravity","gravity_",vars)`

`vars<-gsub("Acc","accelerometer_",vars)`

`vars<-gsub("Gyro","gyroscope_",vars)`

`vars<-gsub("Jerk","derivative_",vars)`

`vars<-gsub("Mag","magnitude_",vars)`

`vars<-gsub("-mean","mean_",vars)`

`vars<-gsub("-std","stdev_",vars)`

\#8.4 remove "()", "-", remove "\_" in the end of the elements

`vars<-gsub("\()","",vars) vars<-gsub("\-","",vars) vars<-gsub("\$","",vars)`

\#8.5 assign descriptive variable names from "vars" to "dataset5"

`names(dataset5)<-vars`

\#8.6 copy "dataset5" to "dataset1" and "dataset2"

`dataset1<-dataset5`

`dataset2<-dataset5`

\#8.7 remove all unused datasets

`rm(dataset3,dataset4,dataset5,testingset,trainingset,variables,vars)`

\#9 calculate average of each measurement for each activity and subject

\#9.1 create variable "activity_subject_id" by combining
"activity_description" and "subject_id" to get unique identifiers

`dataset2$activity_subject_id<-paste(dataset2$activity_description,dataset2$subject_id,sep="_")`

\#9.2 make "activity_subject_id" first column in the dataframe

`dataset2<-relocate(dataset2,"activity_subject_id", .before="activity_description")`

\#9.3 remove unused variables from "dataset2"

`dataset2<-select(dataset2,-activity_description,-subject_id,-set_id,-activity_id)`

\#9.4 group "dataset2" by "activity_subject_id" variable

`dataset2<-group_by(dataset2,activity_subject_id)`

\#9.5 calculate average of each variable in "dataset2" for each
"activity_subject_id" group

`dataset2<-dplyr::summarise(dataset2,across(.cols=everything(),mean,.names="average_{.col}"))`

\#10 create folder "results" in repository and export dataset1 and
dataset2 to this directory as "dataset1.csv" and "dataset2.csv"

`if (!file.exists("results")) { dir.create("results") }`

`if (!file.exists("./results/dataset1.csv")) { write.csv(dataset1,file="./results/dataset1.csv") }`

`if (!file.exists("./results/dataset2.csv")) { write.csv(dataset2,file="./results/dataset2.csv") }`
