# Distracted-Driver-Detection
Driving a car is a complex task, and it requires complete attention. Distracted driving is any activity that takes away the driver’s attention from the road.Our algorithm automatically detects the distracted activity of the drivers and alerts them. We envision this type of product being embedded in cars to prevent accidents due to distracted driving.

There are 10 classes in the dataset:
  - c0 Safe driving.
  - c1 Texting (right hand).
  - c2 Talking on the phone (right hand).
  - c3 Texting (left hand).
  - c4 Talking on the phone (left hand).
  - c5 Operating the radio.
  - c6 Drinking.
  - c7 Reaching behind.
  - c8 Hair and makeup.
  - c9 Talking to passenger(s).
  
This dataset is available on Kaggle, under the State Farm competition: https://www.kaggle.com/c/state-farm-distracted-driver-detection

In order to predict the class, we used VGG-16.
Following is the general proess followed while running different models :

  - Image Augmentation by rotating it and then shifting the width and height of the image. Then only a specific region of the image was taken to further improve               the accuracy of the image.
  - Splitting the data into train, validation and test
  - Running Models by training extra layer first and then all layers
  - Optimizing parameters : number of epochs, batchses and optimizer
  - Running differnt models and repeating the process
  - Ensembling the few selected models

Model has loss: 0.4762 - accuracy: 0.8331 - val_loss: 1.3831 - val_accuracy: 0.7504

## Steps to execute:
  - Data_preprocessing.ipynb: preprocessing of data to input vgg16 model.
  - vgg16.ipynb: training and testing model.
  - Getting the predictions on Video.ipynb
