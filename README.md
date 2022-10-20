#Kaggle Contest to build machine learning models that match radiologists' performance in detecting and localizing fractures in the seven vertebrae of the cervical #spine in CT scans

Submitted by: Aarush Mahajan on 17th October, 2022 

## Project Brief
In this project, I tried to develop a machine-learning model that matches the radiologist’s performance in detecting and localizing fractures to the seven vertebrae that comprise the cervical spine. This project is a part of the Kaggle open-source competition hosted on 28th July 2022. The goal of the competition was to identify fractures in CT scans of the cervical spine (neck) at both the level of a single vertebra and the entire patient. Quickly detecting and determining the location of any vertebral fractures is essential to prevent neurologic deterioration and paralysis after trauma. This competition made use of a  hidden test in the form of a submission notebook, and scoring was done. Model training was done using GPU from the Kaggle environment 
## Intended Outcome
The submissions for the competition are evaluated using a weighted multi-label logarithmic loss. Each fracture sub-type is its own row for every exam, and the expectation is to predict a probability for a fracture at each of the seven cervical vertebrae designated as C1, C2, C3, C4, C5, C6 and C7.There is also a target column, fractured, indicating the probability of whether a fracture exists at the specified level, all of these in a csv file are then compared with actual values and the corresponding loss is calculated the less the loss the better the model so an attempt has been made to build a Efficient-Net CNN with minimum loss.
## Dataset
Data set used for training and testing the model is an open source dataset available on kaggle (Link: https://www.kaggle.com/competitions/rsna-2022-cervical-spine-fracture-detection/data ) it consists of two csv files train.csv for the training of model and test.csv for testing the model, Train/Test Image data organized with one folder per scan, roughly  having 1,500 scans in the hidden test set. Each image is in the dicom file format. The DICOM image files are ≤ 1 mm slice thickness, axial orientation, and bone kernel. Note that some of the DICOM files are JPEG compressed and lastly a sample_submission.csv which would be a valid sample submission.
## Technology 
EfficientNet is one of the most solid baselines known today. It is a family of convolutional neural networks that have achieved state-of-the-art accuracy on ImageNet while also being smaller and faster than other models. The main idea of EfficientNet is scaling up CNNs in a principled way. It uses a scalable architecture, named compound scaling, which balances network depth, width, and resolution to achieve superior performance. The image below shows the scaling method in more detail.


The compound scaling method is based on the idea of balancing dimensions of width, depth, and resolution by scaling with a constant ratio. The equations below show how it is achieved mathematically,


## Project – Outcome &  Learnings
In this project, I trained and evaluated deep learning-based EfficientNet CNN. The presented EfficientNet CNN has the potential to help radiologists during clinical routines and help for detecting cervical spine. The error/score for the trained model is 0.56. EfficientNet CNN's decisions can be followed by inspection of individual lesion scores and box predictions, which is an advantage over other techniques. As there is still a scope of better accuracy, in future work it has to be investigated if it is sufficient to train with a larger dataset, or if an auxiliary CNN is needed to identify abnormal cases and react correspondingly. With advances in healthcare digitization, information about data may also be available in machine-readable form soon. Such information, stored in patient records, may be used to alter the EfficientNet CNNs decision.


