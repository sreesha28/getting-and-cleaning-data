Source Data

The source data is divided in the following way:

'features.txt': List of all the names of features (variables).

'activity_labels.txt': Links the class labels with their activity name.

'X_train.txt': Training set.

'y_train.txt': Training labels.

'X_test.txt': Test set.

'y_test.txt': Test labels.

'subject_train.txt' and 'subject_test.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

A full description of the data used in this project can be found at The UCI Machine Learning Repository

The source data for this project can be found here.

Steps to create Tidy Data

The steps to create Tidy data are registered on the script run_analysis.R and will be described here:

Step 1: Merge the training and test sets to create one data set
X_train.txt and X_test.txt were merged to create Features Data y_train.txt and y_test.txt were merged to create Activity Data subject_train.txt and subject_test.txt were merged to create Subject Data

Features, Activity and Subject datas were merged into a single data set: allData

Step 2: Extracts only the measurements on the mean and standard deviation for each measurement.
features.txt was used to get only columns with mean() or std() in their names and reassigned on allData

Step 3: Use descriptive activity names to name the activities in the data set
activity_Labels.txt is used update values with correct activity names on allData.

Step 4: Appropriately label the data set with descriptive variable names
Use gsub function for pattern replacement to clean up the data labels

Step 5: Create a second, independent tidy data set with the average of each variable for each activity and each subject.