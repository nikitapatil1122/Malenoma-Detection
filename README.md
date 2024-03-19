# Malenoma Detection
> Problem statement: To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Its a CNN based image classification project.
- Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis. In this assignment, I am building multiclass classification model using a custom convolutional neural network in TensorFlow. The model can classify images in malignant and benign oncological diseases (Actinic keratosis,Basal cell carcinoma,Dermatofibroma,Melanoma,Nevus,Pigmented benign keratosis,Seborrheic keratosis,Squamous cell carcinoma,Vascular lesion)
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- For Image classification tasks using CNN we first rescale the data from [0, 255] to [0, 1] to standardize it. 
- For Multiclass classification model we used SparseCategoricalCrossentropy which does not need data to be one hot encoded and accuracy metric to measure model performance
- Without using dropout layes and data augmentation, model seems to overfit which can be seen with extemely good training accuracy but bad validation accuracy
- After adding data augmentation and dropout layers we got rid of overfitting but model accuracy was not good due to class imbalance. To solve the class imbalance we generated 500 more images for each class using Augmenter library after which the model accuracy improved
- We also added additional convolutional layer with more filter count and decaying learning rate strategy for adam optimizer to further enhance the model accuracy.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Tensorflow
- Numpy
- Pandas
- Matplotlib
- Scikit-learn
- Augmentor
- PIL
- pathlib
- Os

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements

- This project was inspired by upgrad Malenoma Detection assignment


## Contact
Created by [@nikitapatil1122] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->