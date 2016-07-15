# Getting-and-Cleaning-Data-Project
Purpose

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit:

a tidy data set as described below;
a link to a Github repository with your script for performing the analysis; and
a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md.
You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.

Objectives

tidy.data.R does the following:

Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive activity names.
Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

tidy.data.R downloads the UCI HAR Dataset data set and puts the zip file into my working directrory, where it is unzipped into the UCI HAR Dataset folder.
Then it loads the train and test data sets and appends the two datasets into one data frame using rbind.
Then it extracts just the mean and standard deviation from the features data set using grep.
The script then cleans the column names and applies them to the x data frame.
Then it loads the activities data set and converts the activity names to lower case using tolower. It also removes underscore using gsub. Activity and subject column names are named for y and subj data sets, respectively.
The script merges the three data sets, x, y and subj, then exports it as a txt file into the Project folder in the same working directory, named merged.txt.
The mean of activities and subjects are created in a separate tidy data set which is exported into the Project folder as txt file named average.txt.
str can be used for an easier preview of the two final data sets.
