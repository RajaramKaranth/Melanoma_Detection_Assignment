# Melanoma Detection Assignment
Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion


## Technologies Used
- Python - version 3.10.9
- IPython - version 8.10.0
- pandas - version 1.5.3
- numpy - version 1.23.5
- seaborn - version 0.12.2
- jupyter notebook - version 6.5.2
- Tensorflow - version 2.15.0
- PIL - version 9.4.0
- matpotlib - version 3.7.1
- Augmentor - version 0.2.12



## Conclusions
- This assignment uses a dataset of about 2357 images of skin cancer types. The dataset contains 9 sub-directories in each train and test subdirectories. The 9 sub-directories contains the images of 9 skin cancer types respectively.
- First, built Model 1 which is a Sequential model with rescaling, 3 convolution and 2 Dense layers to accurately detect 9 classes present in the dataset. Trained for 20 epochs. Model was overfitting with training accuracy at 87% while the validation accuracy is at around 52%. A possible reason could be that the model has some symmetry with weights and biases and memorizing them. We will try breaking them in the next iteration.
- Second, built Model 2 which is a Sequential model with Data Augmentation to address model overfitting. A dropout layer was added for the same purpose.This model also has rescaling, 3 convolution, a dropout layer and 2 dense layers.
- There was a significant improvement in the model performance compared to the previous model. With Train and Validation accuracy was around 46% and 45% respectively, the overfitting has been addressed. However, the accuracy was very low. 
- In the next step,  checked whether there is a class imbalance issue in the dataset and address the same. Below were findings 
  - "seborrheic keratosis" class has the least number of samples - 77.
  - Classes, "pigmented benign keratosis" with 462 samples and "melanoma: with 438 samples classes dominate the data in terms proportionate number of samples.
- Used python package known as Augmentor (https://augmentor.readthedocs.io/en/master/) to add more samples across all classes so that none of the classes have very few samples.
- Third, trained Model 3 on the data created using Augmentor. 30 epochs used.
- The model performance  improved from the previous model in terms of model accuracy. While the training accuracy imporved to 95%, the validation accuracy improved to 80%.
- However, the validation loss is also showed the increasing trend.
- From the explanations offered in different forums, it could be the case of model not learning some classes well which is contributing to the increase in the loss.



## Acknowledgements
Give credit here.
- This project was based on the learnings from Convolutional Neural Networks module of ML C54 EPGP program by IIIT Bangalore and upGrad


## Contact
Created by [@RajaramKaranth] - feel free to contact me!


