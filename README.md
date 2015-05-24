# Cleaning_Data_Project
Getting and Cleaning Data Project
This repository contains the following:

* R Script to read and summarise data from Human Activity Recognition Using Smartphones
* Code Book detailing the Dataset created by the run_analysis.R script


The raw original data (and descirptions of the data) for  this analysis  are avilable at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones  


R Script:
Dependencies/Pre-requisites for running the script:

* The run_analysis.R file is the only script required to repeatably perform the same summarization. 
* The script requires the following libraries:
    * dplyr
* Assumes the data zip file has been unzipped and the following files exist in the current directory :
      *     features.txt            
      *     activity_labels.txt     
      *     /test/X_test.txt        
      *     /test/y_test.txt
      *     /test/subject_test.txt
      *     /train/X_train.txt
      *     /train/y_train.txt
      *     /train/subject_train.txt
      For descriptions of the data in these files, refer to the readme in the zipfile   


The run_analysis.R file was created and tested using R Version 3.2 (32 bit) on a Windows 7 desktop.


The script does the following :
*  Requires/loads  pre-requisite R package
*  Verifies that the raw data files exist in the current working directory along with the subdirectories for train and test datasets.
*  Load the raw data into R Data Frames:
      * Train and Test measurement files
      * subject file for Train and Test Data (which identifies the  ID of the subject in the observation)
      * Activity file for Train and Test Data (which identify the acticity the subject performed while the observations were measured)
      * Activity Label file (Mapping Activity Label like Walking /Laying to the factor values included in measurement files
      * Features file (Listing feature column names of the columns in the measurement file (Columns 3 to 561)
      * 
*  



