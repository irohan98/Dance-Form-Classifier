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

