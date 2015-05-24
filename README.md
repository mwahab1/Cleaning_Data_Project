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
      *     features.txt            ---Names of Feature Columns that have been recorded in the original raw data  
      *     activity_labels.txt     ---Activity Lables (Walking/Laying etc
      *     /test/X_test.txt        ---
      *     /test/y_test.txt
      *     /test/subject_test.txt
      *     /train/X_train.txt
      *     /train/y_train.txt
      *     /train/subject_train.txt
      *     

Other

The script does the following :
*  Requires/loads  pre-requisite R package



