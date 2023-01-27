# IMU_gait_speed_classification
A deep learning approach for classifying gait speed using signals recorded from IMUs

### Introduction:
Gait speed (i.e., the time it takes to ambulate over a certain distance) is an important predictor of aging, pathology, or injury. As people age or suffer from a musculoskeletal disorder, they typically walk slower. Typically, gait speed is collected in a laboratory environment using timing gaits and other similar equipment. Wearable sensors such as inertial measurement units (IMUs), offer an alternative option for recording and analyzing gait outside of a laboratory environment. Classifying gait speed using wearable sensors could be a viable option for longitudinally monitoring gait speed.

This dataset came from an open-source repository with data from multiple wearable sensors. The data was collected by Miraldo, Watanabe, and Duarte at the Federal University of ABC in Brazil. In short, the data was collected at three different walking speed (slow, comfortable, and fast) on 22 healthy adults (publicly available here: https://figshare.com/articles/dataset/Dataset_of_gait_and_inertial_sensors/7778255/3). Sensors were fastened to the shanks and feet of the subjects, and they were instructed to walk at a specified speed over a level overground walking surface.

The goal of this project is to classify different walking speeds using signals derived from IMUs such as angular velocities and/or linear accelerations. More details on the research question and objectives can be found below.


### Research Question
Gait speed is an important factor for gait analysis experiments as it is an important predictor of aging/pathology and can also alter joint kinematics and kinetics. Gait is typically analyzed in a laboratory setting, however, the clinical translatability of these methods is limited because clinicians cannot usually access the equipment, personell, or time required for typical gait analysis. Wearable technology such as IMUs are a popular and alternative option for measuring movement during gait. IMUs are much more affordable, user friendly, and can be used outside of a lab environment. Therefore, the main objective of this project is to analyze signals from IMUs (accelerations and/or angular velocities) at a variety of gait speeds during walking tasks. Specifically, a deep learning model will be trained to classify various gait speed using IMU signals as input. This could be a viable model for assessing gait outside of a laboratory environment and contribute to gait analysis research. 


### Dataset:
* All data was downloaded from the open source repository on figshare (https://doi.org/10.6084/m9.figshare.7778255.v3) provided by Miraldo et al. 
* Reference to data collection methods: https://journals.humankinetics.com/view/journals/mcj/24/4/article-p558.xml


### Repository contents:
* Data:
  * 
