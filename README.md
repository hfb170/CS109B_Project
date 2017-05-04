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
  
  


