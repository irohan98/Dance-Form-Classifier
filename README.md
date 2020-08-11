# Dance-Form-Classifier
### Hi there! 👋
This was my first time participating in a competition and it was a great experience!
## Problem Statement
This International Dance Day, an event management company organized an evening of Indian classical dance performances to celebrate the rich, eloquent, and elegant art of dance. After the event, the company plans to create a microsite to promote and raise awareness among people about these dance forms. However, identifying them from images is a difficult task.

You are appointed as a Machine Learning Engineer for this project. Your task is to build a deep learning model that can help the company classify these images into eight categories of Indian classical dance.

The eight categories of Indian classical dance are as follows:

- Manipuri
- Bharatanatyam
- Odissi
- Kathakali
- Kathak
- Sattriya
- Kuchipudi
- Mohiniyattam

## Dataset Development
Dataset Development- Based on the amount of available data in the training set provided, I have employed multiple data augmentation techniques to further improve the number of examples for each dance form in the dataset. 
To keep a track of the performance and to avoid overfitting problems of the model, I have divided the dataset(only train folder) into a train/val split (80:20) with the augmented dataset.
- training examples - 291    
- test examples     - 73

## Approach 1 (Own Model)

## Approach 2 (Transfer Learning)
The approach used to solve this problem is the transfer learning approach using the VGGNet pre-trained model along with a self-defined softmax layer that is used to classify the 8 different forms of dance present in the dataset.

<p align="center">
    <img src="imagenet_vgg16.png">
</p>

<p align="center">Source: www.google.com</p>

Layers appended after the Pre-trained Model-
- x = Flatten()(vgg.output)
- x = Dense(1024, activation = 'relu')(x)
- x = Dropout(0.20)(x)
- prediction = Dense(8, activation='softmax')(x)

## Techniques Used
rescale = 1/255.0,
    rotation_range = 20,
    zoom_range = 0.2,
    width_shift_range = 0.2,
    height_shift_range = 0.2,
    shear_range = 0.2,
    horizontal_flip = True

## Tools and Libraries
- keras
- tensorflow
- sklearn
- numpy
- pandas
- matplotlib
- os 
- cv2

## Environment
Google Colaboratory

## Model Architecture

## Final Result
- Score- 62.67330 
- Model has been trained for a total of 40 epochs with a batch size=32



<!--
**irohan98/irohan98** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
