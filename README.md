# Getting and Cleaning Data : Project

This repository contains the following:

* R Script to read and summarise data from Human Activity Recognition Using Smartphones
* Code Book detailing the Dataset created by the run_analysis.R script


The raw original data (and descriptions of the data) for  this analysis  are avilable at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones  


#R Script: Dependencies
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



# R Script -  Details
The script does the following :
*  Requires/loads  pre-requisite R package
*  Verifies that the raw data files exist in the current working directory along with the subdirectories for train and test datasets.
*  Load the raw data into R Data Frames:
      * Train and Test measurement files
      * subject files for Train and Test Data (which identifies the  ID of the subject in the observation)
      * Activity files for Train and Test Data (which identify the activity the subject performed while the observations were measured)
      * Activity Label file (Mapping Activity Labels like Walking /Laying to the factor values included in measurement files)
      * Features file (Listing feature column names of the columns in the measurement file (Columns 3 to 561))
      
*  In the Train and Test datasets, remove columns that do not are not indicated as means or standarddeviation observations. For this, only observation columns that have names with one of the following strings are included : mean,Mean,std.
<u> Please note that according to the Community TA (David Hood - many thanks)  posting in the forum at (https://class.coursera.org/getdata-014/forum/thread?thread_id=31#comment-519) the actual list of columns chosen is not a marking criterion. In my opinion, not knowing the underlying data, it was best to chose all data columns that had mean/std/Mean in their column names, including some that were meanFreq etc.</u>

*  Combine the subject, activity and measurements columns to create one Train Dataset as an R data frame.
*  Combine the subject, activity and measurements columns to create one Test Dataset as an R data frame.
*  Combine the Train and Test data frame into one comprehensive data frame
*  Replaces the Acitivy IDs (1,2..6) in the combined data frame using text descriptors from activity_lables.txt file(WALKING, WALKING_UPSTAIRS etc). In this process , it also converts the activity column into a factor.
*  The column names of this dataset are then replaced with more descriptive column names.
*  Finally a mean of each variable is calculated for each activity and each subject. 
*  This final tiday dataset is then written out to a text file called Tidy_Samung.txt


#Reading Tidy Data into R
df_readdata_txt<- read.table("Tidy_Samsung.txt", header=TRUE)





