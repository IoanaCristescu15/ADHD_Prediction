# ADHD-Prediction


# RUN jupyter notebook
DataCleaning
surveyHistogram
sensorHistogram
CreateDataset
FeatureExtraction
machineModels 
featureVisual
Correlation


# CSV Files
Activity1
Activity2
Activity_clean1
Activity_clean2
Activity_joined
sassema_updated_weekly
weekly_data_for_visualization
sassema baseline 3.16.2023
Activity_clean
Feature_mapping
Upscaling





# Functions of jupyter notebooks and results in csv files explained 
This readme files serves as a guide to explain the functions of all jupyter notebooks and results in csv files. 

In DataCleaning:

We started the data pre-processing step by combing Activity1.csv with Activity2.csv, representing data collected from Phase 1 and Phase 2 of the collection process. 

We then clean the duplicates, and put the results in Activity_clean1.csv and Activity_clean2.csv. We put the combined clean data into Activity_joined.csv

In surveyHistogram :
We extraced 18 questions from sassema_updated_weekly.csv  The questions are combined and put into weekly_data_for_visualization.csv. We calculated the intervals between weekly surveys and established the thresholds as discussed in the report. 


In sensorHistogram:
We calculated the sensing data days between 2 surveys and established the thresholds as discussed in the report. We added the baseline date from baseline data from sassema baseline 3.16.2023.csv.



In CreateDataset:

Based on Activity_joined.csv and results from the histograms, we created Activity_clean.csv. We removed the survey dates under the threshold, added the baseline date. We also added the ADHD label and ADHD scores. ADHD scores are calculated from 18 questions extracted. 


In FeatureExtraction:
(more details are in StillFeatures and RunningFeatures)
We calculate 8 features based on Activity_clean.csv, added the ADHD label and ADHD Score, and Survey Dates. The new data frame is put into feature_mapping.csv. We upscaled the dataset in excel, and put into upscaling.csv.


In machineModels:
Running all ML models on upscaling.csv. 

In featureVisual:
Using upscaling.csv, we visualize the features for both ADHD participants and non-ADHD participants.

In Correlation:
Using Upscaling.csv, we calculated Pearson Correlations for the features. 

