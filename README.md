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
The data folder consists of two folders and two .csv files. The details are as follows:

- train: Contains 364 images for 8 classes ['manipuri','bharatanatyam','odissi','kathakali','kathak','sattriya','kuchipudi','mohiniyattam']
- test: Contains 156 images
- train.csv: 364 x 2
- test.csv: 156 x 1

Based on the amount of available data in the training set provided, I have employed multiple data augmentation techniques to further improve the number of examples for each dance form in the dataset. 
To keep a track of the performance and to avoid overfitting problems of the model, I have divided the dataset(only train folder) into a train/val split (80:20) with the augmented dataset.
- training examples - 291    
- test examples     - 73

## Approach 1 (Own Model)
This approach was a model made from scratch. The layers that were defined are mostly similar to the layers of the CNN used for the Fashion_MNIST dataset. This approach will get you familiar with the behaviour of the CNN with the Dataset and give you an idea of "What Exactly is Happening!" when you add/remove layers and train the model for a few epochs. 

## Approach 2 (Transfer Learning)
The approach used to solve this problem is the transfer learning approach using the VGGNet pre-trained model along with a self-defined softmax layer that is used to classify the 8 different forms of dance present in the dataset.

<p align="center">
    <img src="imagenet_vgg16.png">
</p>

<p align="center">Source: https://neurohive.io/en/popular-networks/vgg16/</p>

Layers appended after the Pre-trained Model-
- x = Flatten()(vgg.output)
- x = Dense(1024, activation = 'relu')(x)
- x = Dropout(0.20)(x)
- prediction = Dense(8, activation='softmax')(x)

## Techniques Used
- rescale = 1/255.0,
- rotation_range = 20,
- zoom_range = 0.2,
- width_shift_range = 0.2,
- height_shift_range = 0.2,
- shear_range = 0.2,
- horizontal_flip = True

The above values can be varied and can be experimented with.

## Tools and Libraries
- keras
- tensorflow (2.x)
- tensorboard
- sklearn 
- numpy
- pandas
- matplotlib
- os 
- cv2

## Model Architecture
You can see the architecture of the model in the above colab notebook using the code shown below
```
model.summary()
```

## Environment
Google Colaboratory

## Evaluation metric
- score = {100* f1\_score(actual\_values,predicted\_values,average = 'weighted')}

## Final Result
- Competition Score- 58.53426 (using approach 2) 
- Model has been trained for a total of 40 epochs with a batch size = 32 

I got a rank of 409/5864 (Top 6.9%) for the model that I have developed. Still a long way to go! 😄

https://www.hackerearth.com/challenges/competitive/hackerearth-deep-learning-challenge-identify-dance-form/leaderboard/identify-the-dance-form-deea77f8/page/9/

**Hope you enjoyed going through my analysis! 😄**



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
