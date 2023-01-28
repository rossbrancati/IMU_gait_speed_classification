# IMU_gait_speed_classification
A deep learning approach for classifying gait speed using signals recorded with IMUs

### Introduction:
Gait speed (i.e., the time it takes to ambulate over a certain distance) is an important predictor of aging, pathology, or injury. As people age or suffer from a musculoskeletal disorder, they tend to walk slower. Typically, gait speed is collected in a laboratory environment using timing gaits and other similar equipment. Wearable sensors such as inertial measurement units (IMUs), offer an alternative option for recording and analyzing gait outside of a laboratory environment. Classifying gait speed using wearable sensors could be a viable option for measuring and longitudinally monitoring gait speed.

This dataset came from an open-source repository with data from multiple wearable sensors. The data was provided by Miraldo, Watanabe, and Duarte from the Federal University of ABC in Brazil. In short, the data was collected at three different walking speed (slow, comfortable, and fast) on 22 healthy adults (publicly available here: https://figshare.com/articles/dataset/Dataset_of_gait_and_inertial_sensors/7778255/3). Sensors were fastened to the shanks and feet of the subjects, and they were instructed to walk at a specified speed over a level overground walking surface.

The goal of this project is to classify different walking speeds using signals derived from IMUs such as angular velocities and/or linear accelerations. More details on the research question and objectives can be found below.


### Research Question
Gait speed is an important factor for gait analysis experiments as it is an important predictor of aging/pathology and can also alter joint kinematics and kinetics. Gait is typically analyzed in a laboratory setting, however, the clinical translatability of these methods is limited because clinicians cannot usually access the equipment, personell, or time required for typical gait analysis. Wearable technology such as IMUs are a popular and alternative option for measuring movement during gait. IMUs are much more affordable, user friendly, and can be used outside of a lab environment. Therefore, the main objective of this project is to analyze signals from IMUs (accelerations and/or angular velocities) at a variety of gait speeds during walking tasks. Specifically, a deep learning model will be trained to classify various gait speed using IMU signals as input. This could be a viable model for assessing gait outside of a laboratory environment and contribute to gait analysis research. 


### Dataset:
* All data was downloaded from the open source repository on figshare (https://doi.org/10.6084/m9.figshare.7778255.v3) provided by Miraldo et al. 
* Reference to data collection methods: https://journals.humankinetics.com/view/journals/mcj/24/4/article-p558.xml


### Repository contents:

#### notebooks:
* pre_processing.ipynb - the pre-processing steps to get from the original data to a structure ready for training models
* IMU_gait_speed_classification_DL_modeling.ipynb - development of the DL model
* IMU_gait_speed_classification_google_colab.ipynb - a notebook developed in Google Colab that I used to train the model online Colab's GPU.
* IMU_gait_speed_classification_exploratory.ipynb - a notebook that contain the initial steps I used to explore data, feature engineer, and try other ML models before I landed on the deep learning approach. 


### Instructions for pre-processing the data
* The following steps will walk through taking the data from the repository and getting it into a format that is usable for training models
1) Download all data from the open source repository (https://doi.org/10.6084/m9.figshare.7778255.v3). Save it in a folder titled "data"
2) Use the pre_processing.ipynb notebook to restructure and standardize the data. You may need to change file paths depending on where you store the data and notebook files. You will also need to create empty folders to store the data. 
3) The end result of using pre_processing.ipynb will be the following files: 
* "RS_ML_matrix.csv" and "LS_ML_matrix.csv" - restructured data (not standardized) where each row is a stride (12102 total strides) and each column is a timepoint of the gait cycle for a signal (6 signals * 101 timepoints per signal = 606 total features). Subject ID, trial number, and speed are also in these files. 
* "RS_ML_matrix_std.csv" and "LS_ML_matrix_std.csv" - the same files, but standardized using a z-transformation (eventually used for the training deep learning model)


### Instructions for other notebooks:
* The exploratory notebook is where I started with pre-processing the data, running some simple classifiers, extracting statistical features and principal components, and ultimately landing on a deep learning approach. Check out this notebook if you are interested in where to start when working with a new dataset. 
* IMU_gait_speed_classification_DL_modeling.ipynb is where I created the original deep learning model used in the google colab notebook. If you're interested in how I created the model, check out this notebook. It has some similarities with the exploratory notebook. 
* IMU_gait_speed_classification_google_colab.ipynb - if you are just interested in training and testing the deep learning model using leave one subject out cross validation, run this notebook in google colab (instructions in notebook). The input data is "RS_ML_matrix_std.csv", but you can use other files as well such as the left shank or non-standardized data.

### Once you have the data pre-processed and into the format for the deep learning model, you can run it through the google colab notebook

