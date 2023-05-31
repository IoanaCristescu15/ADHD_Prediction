# ADHD-Prediction
Authors: Ioana Cristescu and Ying Zhu <br/>

# Paper:
For a better understanding of the project and processes read the paper ADHD_Prediction.pdf.

# Direction for compiling:
Run the Jupyter notebooks in the following order <br/>
DataCleaning.ipynb <br/>
surveyHistogram.ipynb <br/>
sensorHistogram.ipynb <br/>
CreateDataset.ipynb <br/>
FeatureExtraction.ipynb <br/>
machineModels.ipynb  <br/>
featureVisual.ipynb <br/>
Correlation.ipynb <br/>

# Design Decisions: 
This readme files serves as a guide to explain the functions of all Jupyter notebooks and results in csv files. 

## DataCleaning:
We start the data pre-processing step by combing Activity1.csv with Activity2.csv, representing data collected from Phase 1 and Phase 2 of the collection process.  <br/> 
We then clean the duplicates, and save the results in Activity_clean1.csv and Activity_clean2.csv. We combine the cleaned data into Activity_joined.csv

## surveyHistogram :
We extract 18 questions from sassema_updated_weekly.csv. The questions are combined and saved into weekly_data_for_visualization.csv. We calculate the intervals between weekly surveys and established the thresholds as discussed in the report. 


## sensorHistogram:
We calculate the sensing data days between 2 surveys and established the thresholds as discussed in the report. We add the baseline date from baseline data from sassema baseline 3.16.2023.csv.



## CreateDataset:
Based on Activity_joined.csv and results from the histograms, we creat Activity_clean.csv. We remove the survey dates under the threshold and add the baseline date. We also add the ADHD label and ADHD scores. ADHD scores are calculated from the 18 questions extracted. 


## FeatureExtraction:
(more details are in StillFeatures.ipynb and RunningFeatures.ipynb) <br/> 
We calculate 8 features based on Activity_clean.csv and add the ADHD label and ADHD Score, and Survey Dates. The new data frame is saved into feature_mapping.csv. We upscale the dataset and save into upscaling.csv.


## machineModels:
Running all ML models on upscaling.csv. 

## featureVisual:
Using upscaling.csv, we visualize the features for both ADHD participants and non-ADHD participants.

## Correlation:
Using Upscaling.csv, we calculate Pearson Correlations for the features. 

