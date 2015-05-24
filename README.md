# Getting and Cleaning Data : Project

This repository contains the following:

* R Script to read and summarise data from Human Activity Recognition Using Smartphones
* Code Book detailing the Dataset created by the run_analysis.R script


The raw original data (and descriptions of the data) for  this analysis  are avilable at the following locations: 
* http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones  
* https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

##R Script: Dependencies
Dependencies/Pre-requisites for running the script:

* The run_analysis.R file is the only script required to repeatably perform the same summarization. 
* The script requires the following libraries:
    * dplyr
* Script assumes the data zip file has been unzipped and the following files exist in the current directory :
      *     features.txt            
      *     activity_labels.txt     
      *     /test/X_test.txt        
      *     /test/y_test.txt
      *     /test/subject_test.txt
      *     /train/X_train.txt
      *     /train/y_train.txt
      *     /train/subject_train.txt
      For descriptions of the data in these files, refer to the readme in the zipfile.  

<em>The run_analysis.R file was created and tested using R Version 3.2 (32 bit) on a Windows 7 desktop.</em>



## R Script -  Details
The script does the following :
*  Requires/loads  pre-requisite R package
*  Verifies that the raw data files exist in the current working directory along with the subdirectories for train and test datasets.
*  Load the raw data into R Data Frames:
      * Train and Test measurement files
      * subject files for Train and Test Data (which identifies the  ID of the subject in the observation)
      * Activity files for Train and Test Data (which identify the activity the subject performed while the observations were measured)
      * Activity Label file (Mapping Activity Labels like Walking /Laying to the factor values included in measurement files)
      * Features file (Listing feature column names of the columns in the measurement file (Columns 3 to 561))
      
*  In the Train and Test datasets, remove columns that are not indicated as means or standarddeviation observations. For this, only observation columns that have names with one of the following strings are included : mean,Mean,std.
<b> Please note that according to the Community TA (David Hood - many thanks)  posting in the forum at (https://class.coursera.org/getdata-014/forum/thread?thread_id=31#comment-519) the actual list of columns chosen is not a marking criterion. Not knowing the underlying data, it was best to chose all data columns that had mean/std/Mean in their column names, including some that were meanFreq etc. This minimises the chances that some required columns are dropped accidentally- resulting in adverse data loss</b>

*  Combine the subject, activity and measurements columns to create one Train Dataset as an R data frame.
*  Combine the subject, activity and measurements columns to create one Test Dataset as an R data frame.
*  Combine the Train and Test data frame into one comprehensive data frame
*  Replaces the Acitivy IDs (1,2..6) in the combined data frame using text descriptors from activity_lables.txt file(WALKING, WALKING_UPSTAIRS etc). In this process , it also converts the activity column into a factor.
*  The column names of this dataset are then replaced with more descriptive column names. (Note that the requirement to make all column names lower case is not mandatory according to lecture notes last slide of (http://jtleek.com/modules/03_GettingData/04_01_editingTextVariables/#1). IN this case...the column names woul have been very long and confusing without some capitalization. 
*  Finally a mean of each variable is calculated for each activity and each subject. 
*  This final tiday dataset is then written out to a text file called Tidy_Samung.txt



##Steps to reading Tidy Data (Tidy_Samsung.txt) into R 
* <b>Option 1: After downloading data file locally to current working directory of R</b>

df_data <- read.table("Tidy_Samsung.txt", header=TRUE)

* <b>Option 2: Reading  data file from the submission URL directly:</b>

df_data <- read.table(
      "https://s3.amazonaws.com/coursera-uploads/user-e40aa5dc398627b4ba751caf/973501/asst-3/bac7b720025311e5aa668f13681ea683.txt",
      header=TRUE)




