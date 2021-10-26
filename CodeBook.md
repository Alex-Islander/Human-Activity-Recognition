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