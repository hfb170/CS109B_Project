# CS109B_Project
CS109B Group Project

Group project for CS109B - Spring 2017

This repository should be as divided into two partitions. The first partition is the folder "Project Codes" which is meant to be the deliverable material of this repository while the second is the rest of the folders are mainly one folder per milestone and folder for the file used to produce visualizations or from which other project visualizations were implemented. This material is also exixtent in another repository with the following link:

https://github.com/nina-ifti/CS109B_Project_Group26.git

## Focusing on the Project code folder:

The folder include four subdirectories which are \:

 - Data acquisition
 - Data exploration and pre-processing
 - Conventional models
 * Neural models
 
 The following presentation of the different files is respecting the chronological evolution of the analysis pursued for the project

### Data Acquisition:

This folder includes the files that were used initially to scrap the data from the database sites. 

- We start by the file "info.ipynb" which simply explore the site fro valid movie IDs. Thsi was important as based on the preliminary  
  study, it was found that the movie ID is the most important key to relate to different attributes in the data
  
- The file "DataTMDB.ipynb" is the most important file used to scrap all the meta data required in addition to the genres and the poster path

- The file "PosterAcquisition.ipynb" was the file used to acquire the poster based on the poster path already scraped by the previous model

### Data Exploration and pre-processing:

This folder includes the following files:

 - EDAIDMB5000 which was a preliminary data exploration work performed by tableau once we got acces to the data base
 - The file "Genrpairs.ipynb" was used to calculate the frequencty of genre pair occurrences in both the IMDB and the TMDB databases. This was a requirement for the first Milestone
 
 - The file "GenresExtraction.ipynb" was developped to encode the movie genres and construct an encoded array to be used with the different classifiers
 
 - The file "PosterProc.ipynb" was developped as a second stepafter the poster acquisition. This file extract the color statistics as features that can be used for classification. This was needed for Milestone 3 modeling work and for the Neural Models as an additional input for certain characteristics
 
  - As the file "PosterProc.ipynb" was necessary for the conventional models, the file "PosterProcNN.ipynb" was necessary for the Deep Learniing models. This file transform the poster image into a numerical array that can be handled by different network architectures
  
  
### Conventional Models:

Pursuant to all the data preparation work presented above, the modeling work was tackled in Milestones from 3 to 5. This folder include the files that covers the following models investigated by the team

 - Logistic regression based on the overview/keywords NLP (CS109B_LogReg_updated.Rmd)
 - Logistic regression based on the color statistics (datasci_DD_logit.Rmd)
 - SVM based on the color statistics (datasci_DD_svm.Rmd)
 - The random forest and addaboost applied on all the acquired features (Random_Forest_Decision_Tree_Gradient_Boosting_cs109b (1).ipynb)

### The neural models

Finally the deep learning models which is partitioned into two main folders, the training folder and the test folder.

- The training folder includes a subfolder for each architecture that includes the code file, the exported h5 model and the accumulated accurracy during the training as a csv file

- The test folder include one folder for the basic CNNarchitecture variants that includes a generic code used for evaluation in addition to two data file per each varianat. The first is the predicted probability and the second is the calculated proximity distance as a derived metric to be used for visualization

 - The other folders are structured as a single folder for each architecture that has the same file structure which is a code for the evaluation of the test prediction and two data files:one for the predicted probability and the second for the metric used for visualization
 
 - In addition a last folder "Analysis" which was the last to be introduced. This folder includes all the acquired prediction data and metrics that was subsequently used by the file "CS109b-project_DL_Viz.Rmd" to produce the necessary visualizations

