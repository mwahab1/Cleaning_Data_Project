# CodeBook for Cleaning Data Project

This code book has the following sections:
* Background
* Source of raw data and desciption of data collection methods   
* Transformation performed on raw data to obtain the data set in the Tidy dataset
* Variables in data set 

###Background

The Tidy data file created from the raw data follows some of the precepts laid down in the following sources:
* Hadley Wickham (http://vita.had.co.nz/papers/tidy-data.pdf)
* Jeff Leek (https://github.com/jtleek/datasharing)

### Source of Raw Data 

The raw data for this is available at: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 
and https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

These links also provide  descrptions of underlying data capture and processing.  

### Transformtions Performed on Raw Data
* The raw data in zipfile was downloaded and unzipped using MS Windows Extraction.
* The files were then loaded into R and a Tidy DataSet created using the run_analysis.R script in this repository

Readme.md has details on the run_analysis.R script.


###Data /Variables in Tidy Data file.
* subject: integer from 1 to 30 representing each unique human subject in the study 
* activity: Character string. Values:
    * WALKING
    * WALKING_UPSTAIRS
    * WALKING_DOWNSTAIRS
    * SITTING
    * STANDING
    * LAYING
    
The rest of the measures all have the following characteristics:
a) they are numeric in the range of -1 to +1  b) they are averages from the raw data per subject , activity combination as described in the processing section.

* TimeBodyAccelerationmeanXAxis (Mean Time Body Acceleration mean - X Axis)
* TimeBodyAccelerationmeanYAxis (Mean Time Body Acceleration mean - Y Axis)
* TimeBodyAccelerationmeanZAxis (Mean Time Body Acceleration mean - Z Axis)
* TimeBodyAccelerationstandarddeviationXAxis (Mean of Time Body Acceleration Standard Deviation - X Axis) 
* TimeBodyAccelerationstandarddeviationYAxis (Mean of Time Body Acceleration Standard Deviation - Y Axis) 
* TimeBodyAccelerationstandarddeviationZAxis (Mean of Time Body Acceleration Standard Deviation - Z Axis)
* TimeGravityAccelerationmeanXAxis (Mean Time Gravity Acceleration mean - X Axis)
* TimeGravityAccelerationmeanYAxis (Mean Time Gravity Acceleration mean - Y Axis)
* TimeGravityAccelerationmeanYAxis (Mean Time Gravity Acceleration mean - Y Axis)
* TimeGravityAccelerationstandarddeviationXAxis (Mean of Time Gravity Acceleration Standard Deviation - X Axis
* TimeGravityAccelerationstandarddeviationYAxis (Mean of Time Gravity Acceleration Standard Deviation - Y Axis
* TimeGravityAccelerationstandarddeviationZAxis (Mean of Time Gravity Acceleration Standard Deviation - Z Axis
* TimeBodyAccelerationJerkmeanXAxis (Mean Time Body Acceleration Jerk mean - X Axis)
* TimeBodyAccelerationJerkmeanYAxis (Mean Time Body Acceleration Jerk mean - Y Axis)
* TimeBodyAccelerationJerkmeanZAxis (Mean Time Body Acceleration Jerk mean - Z Axis)
* TimeBodyAccelerationJerkstandarddeviationXAxis (Mean Time Body Acceleration Jerk standard deviation - X Axis)
* TimeBodyAccelerationJerkstandarddeviationYAxis (Mean Time Body Acceleration Jerk standard deviation - Y Axis)
* TimeBodyAccelerationJerkstandarddeviationZAxis (Mean Time Body Acceleration Jerk standard deviation - Z Axis)
* TimeBodyGyroscopemeanXAxis (Mean Time Body Gyroscope mean - X Axis)
* TimeBodyGyroscopemeanYAxis (Mean Time Body Gyroscope mean - Y Axis)
* TimeBodyGyroscopemeanZAxis (Mean Time Body Gyroscope mean - Z Axis)
* TimeBodyGyroscopestandarddeviationXAxis (Mean Time Body Gyroscope Standard Deviation - X Axis)
* TimeBodyGyroscopestandarddeviationYAxis (Mean Time Body Gyroscope Standard Deviation - Y Axis)
* TimeBodyGyroscopestandarddeviationZAxis (Mean Time Body Gyroscope Standard Deviation - Z Axis)
* TimeBodyGyroscopeJerkmeanXAxis (Mean Time Body Gyroscope Jerk mean - X Axis)
* TimeBodyGyroscopeJerkmeanYAxis (Mean Time Body Gyroscope Jerk mean - Y Axis)
* TimeBodyGyroscopeJerkmeanZAxis (Mean Time Body Gyroscope Jerk mean - Z Axis)
* TimeBodyGyroscopeJerkstandarddeviationXAxis (Mean Time Body Gyroscope Jerk standard deviation - X Axis)
* TimeBodyGyroscopeJerkstandarddeviationYAxis (Mean Time Body Gyroscope Jerk standard deviation - Y Axis)
* TimeBodyGyroscopeJerkstandarddeviationZAxis (Mean Time Body Gyroscope Jerk standard deviation - Z Axis)
* TimeBodyAccelerationMagnitudemean (Mean Time Body Acceleration Magnitude mean)
* TimeBodyAccelerationMagnitudestandarddeviation (Mean Time Body Acceleration Magnitude Standard Deviation)
* TimeGravityAccelerationMagnitudemean (Mean Time Gravity Acceleration Magnitude mean)
* TimeGravityAccelerationMagnitudestandarddeviation (Mean Time Gravity Acceleration Magnitude mean)
* TimeBodyAccelerationJerkMagnitudemean (Mean Time Body Acceleration Jerk Magnitude mean)
* TimeBodyAccelerationJerkMagnitudestandarddeviation (Mean Time Body Acceleration Jerk Magnitude Standard Deviation)
* TimeBodyGyroscopeMagnitudemean (Mean Time Body Gyroscope Magnitude mean)
* TimeBodyGyroscopeMagnitudestandarddeviation (Mean Time Body Gyroscope Magnitude Standard Deviation)
* TimeBodyGyroscopeJerkMagnitudemean (Mean Time Body Gyroscope Jerk Magnitude mean)
* TimeBodyGyroscopeJerkMagnitudestandarddeviation (Mean Time Body Gyroscope Jerk Magnitude Standard Deviation)
* FrequencyDomainBodyAccelerationmeanXAxis (Mean Frequency Domain Body Acceleration mean - X Axis)
* FrequencyDomainBodyAccelerationmeanYAxis (Mean Frequency Domain Body Acceleration mean - Y Axis)
* FrequencyDomainBodyAccelerationmeanZAxis (Mean Frequency Domain Body Acceleration mean - Z Axis)
* FrequencyDomainBodyAccelerationstandarddeviationXAxis (Mean Frequency Domain Body Acceleration Standard Deviation - X Axis)
* FrequencyDomainBodyAccelerationstandarddeviationYAxis (Mean Frequency Domain Body Acceleration Standard Deviation - Y Axis)
* FrequencyDomainBodyAccelerationstandarddeviationZAxis (Mean Frequency Domain Body Acceleration Standard Deviation - Z Axis)
* FrequencyDomainBodyAccelerationmeanFrequencyXAxis (Mean Frequency Domain Body Acceleration mean Frequency - X Axis)
* FrequencyDomainBodyAccelerationmeanFrequencyYAxis (Mean Frequency Domain Body Acceleration mean Frequency - Y Axis)
* FrequencyDomainBodyAccelerationmeanFrequencyZAxis (Mean Frequency Domain Body Acceleration mean Frequency - Z Axis)
* FrequencyDomainBodyAccelerationJerkmeanXAxis (Mean Frequency Domain Body Acceleration Jerk mean - X Axis)
* FrequencyDomainBodyAccelerationJerkmeanYAxis (Mean Frequency Domain Body Acceleration Jerk mean - Y Axis)
* FrequencyDomainBodyAccelerationJerkmeanZAxis (Mean Frequency Domain Body Acceleration Jerk mean - Z Axis)
* FrequencyDomainBodyAccelerationJerkstandarddeviationXAxis (Mean Frequency Domain Body Acceleration Jerk Std. Deviation - X Axis)
* FrequencyDomainBodyAccelerationJerkstandarddeviationYAxis (Mean Frequency Domain Body Acceleration Jerk Std. Deviation - Y Axis)
* FrequencyDomainBodyAccelerationJerkstandarddeviationZAxis (Mean Frequency Domain Body Acceleration Jerk Std. Deviation - Z Axis)
* FrequencyDomainBodyAccelerationJerkmeanFrequencyXAxis (Mean Frequency Domain Body Acceleration Jerk mean Frequency - X Axis)
* FrequencyDomainBodyAccelerationJerkmeanFrequencyYAxis (Mean Frequency Domain Body Acceleration Jerk mean Frequency - Y Axis)
* FrequencyDomainBodyAccelerationJerkmeanFrequencyZAxis (Mean Frequency Domain Body Acceleration Jerk mean Frequency - Z Axis)
* FrequencyDomainBodyGyroscopemeanXAxis (Mean Frequency Domain Body Gyroscope mean - X Axis)
* FrequencyDomainBodyGyroscopemeanYAxis (Mean Frequency Domain Body Gyroscope mean - Y Axis)
* FrequencyDomainBodyGyroscopemeanZAxis (Mean Frequency Domain Body Gyroscope mean - Z Axis)
* FrequencyDomainBodyGyroscopestandarddeviationXAxis (Mean Frequency Domain Body Gyroscope Standard Deviation - X Axis)
* FrequencyDomainBodyGyroscopestandarddeviationYAxis (Mean Frequency Domain Body Gyroscope Standard Deviation - Y Axis)
* FrequencyDomainBodyGyroscopestandarddeviationZAxis (Mean Frequency Domain Body Gyroscope Standard Deviation - Z Axis)
* FrequencyDomainBodyGyroscopemeanFrequencyXAxis (Mean Frequency Domain Body Gyroscope mean Frequency - X Axis)
* FrequencyDomainBodyGyroscopemeanFrequencyYAxis (Mean Frequency Domain Body Gyroscope mean Frequency - Y Axis)
* FrequencyDomainBodyGyroscopemeanFrequencyZAxis (Mean Frequency Domain Body Gyroscope mean Frequency - Z Axis)
* FrequencyDomainBodyAccelerationMagnitudemean (Mean Frequency Domain Body Acceleration Magnitude mean)
* FrequencyDomainBodyAccelerationMagnitudestandarddeviation (Mean Frequency Domain Body Acceleration Magnitude Standard Deviation)
* FrequencyDomainBodyAccelerationMagnitudemeanFrequency (Mean Frequency Domain Body Acceleration Magnitude mean Frequency)
* FrequencyDomainBodyAccelerationJerkMagnitudemean (Mean Frequency Domain Body Acceleration Jerk Magnitude mean)
* FrequencyDomainBodyAccelerationJerkMagnitudestandarddeviation (Mean Frequency Domain Body Acceleration Jerk Magnitude Standard Deviation)
* FrequencyDomainBodyAccelerationJerkMagnitudemeanFrequency (Mean Frequency Domain Body Acceleration Jerk Magnitude mean Frequency)
* FrequencyDomainBodyGyroscopeMagnitudemean (Mean Frequency Domain Body Gyroscope Magnitude mean)
* FrequencyDomainBodyGyroscopeMagnitudestandarddeviation (Mean Frequency Domain Body Gyroscope Magnitude Standard Deviation)
* FrequencyDomainBodyGyroscopeMagnitudemeanFrequency (Mean Frequency Domain Body Gyroscope Magnitude mean Frequency)
* FrequencyDomainBodyGyroscopeJerkMagnitudemean (Mean Frequency Domain Body Gyroscope Jerk Magnitude mean)
* FrequencyDomainBodyGyroscopeJerkMagnitudestandarddeviation (Mean Frequency Domain Body Gyroscope Jerk Magnitude Standard Deviation)
* FrequencyDomainBodyGyroscopeJerkMagnitudemeanFrequency (Mean Frequency Domain Body Gyroscope Jerk Magnitude mean Frequency)
* angleofTimeBodyAccelerationMeanandGravityMean (Mean Angle of Time Body Acceleration Mean and Gravity Mean)
* angleofTimeBodyAccelerationJerkMeanandGravityMean (Mean Angle of Time Body Acceleration Jerk Mean and Gravity Mean)
* angleofTimeBodyGyroscopeMeanandGravityMean (Mean Angle of Time Body Gyroscope Mean and Gravity Mean)
* angleofTimeBodyGyroscopeJerkMeanandGravityMean (Mean Angle of Time Body Gyroscope Jerk Mean and Gravity Mean)
* angleofXaxisandGravityMean (Mean Angle of X Axis and Gravity Mean)
* angleofYaxisandGravityMean (Mean Angle of Y Axis and Gravity Mean)
* angleofZaxisandGravityMean (Mean Angle of Z Axis and Gravity Mean)


 
