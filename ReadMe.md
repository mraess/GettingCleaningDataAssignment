

### READ ME - Getting and cleaning data assignment (R-script: run_analysis.R)


Human Activity Recognition Using Smartphones Dataset


The run_analysis.R script reads data from the "Human Activity Recognition Using Smartphones Dataset Version 1.0" 
and produces a tidy dataset, which can then be used for further analysis.

The data in the "Human Activity Recognition Using Smartphones Dataset Version 1.0" were produced by
a group of 30 volunteers (ages 19 - 48).

Each person performed six activities: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
wearing a smartphone (Samsung Galaxy S II) on the waist. 

Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz data were captured. 
The experiments were video-recorded to label the data manually. 
The obtained dataset was randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data 
and 30% the test data.

The original dataset included the following data files:

'features.txt': List of all features.

'activity_labels.txt': List of class labels and their activity name.

'train/X_train.txt': Training set.

'train/y_train.txt': Training labels.

'train/subject_train.txt': ID's of subjects in the training data

'test/X_test.txt': Test set.

'test/y_test.txt': Test labels.

'test/subject_test.txt': ID's of subjects in the training data


A brief description of the script:

The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis.

It then reads all required .txt files and labels the datasets

Consquently the appropriate "activity_id"'s and "subject_id"'s are appended to the "test" and the "training" data, which are then combined into one single data frame

Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created

Using the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names

Lastly, with the help of the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy_movement_data.txt" file.

A description of the "tidy_smartphone_activity_data.txt" file can be found in the "CodeBook.md" file.

Acknowledgements:

Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

License:

Use of the run_analysis.R script is free for all users.

Use of the resulting dataset "tidy_smartphone_activity_data.txt" in publications must be acknowledged by referencing:

Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using 
a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

Disclaimer: This dataset is distributed AS-IS! The author does not take any responsibility for another user's use or misuse!!
Any commercial use is prohibited.

