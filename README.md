# Face-Mask-Detector
In this project we have built a face mask detector which helps us to predict whether a person is wearing mask or not and all that in real time via a webcam or video streams. <br/><br/>
This project is specifically divided into two parts i.e.
  1. Creating our dataset and training the face mask detector model.
  2. Applying the trained model to work along with the webcam to give us real time predictions.

## Dataset
Usually what I found in the datasets available on the internet was it generally had two categories mask and without mask. Hence I decided to include another category which would increase the usability and efficiency of our face mask detector. <br/> <br/>
That being said, our dataset has 3 categories of people:
- wearing mask
- not wearing mask
- wearing mask but in an incorrect manner

Each category has close to 600-700 images. Obviously it is not possible to download or web-scrap this many images. Hence **_data augmentation_** technique has been applied on 80-100 images to increase the volume of our dataset. <br/> <br/>
Since the size of the dataset is quite big (~ 200 mb) hence I couldn't commit the dataset here but you can download it from my [kaggle](https://www.kaggle.com/spandanpatnaik09/face-mask-detectormask-not-mask-incorrect-mask) profile. <br/>
(P.S: If you really liked the dataset don't forget to give a thumbs up. Creating dataset is quite a task)

## Training the face mask detector model
Here our face mask dataset is loaded and trained using keras/tensorflow. <br/>
We have fine-tuned [MobileNet V2](https://arxiv.org/abs/1801.04381) model / architecture with pre-trained [ImageNet](http://www.image-net.org/) weights.

## Using the trained model
After training the face mask detector model, it is then loaded to perform face mask detection.

## Scope for improvement
Nothing in this world is perfect and so is our face mask detector. I have listed some aspects of our project which has scope of improvemet.
1. We can notice that all three categories of our dataset has people wearing basic white / blue surgical use and throw masks. While our model works perfectly fine but some times it is unable to detect / predict if any person is wearing printed / designer masks.<br/>
Hence we can experiment by adding more images in our dataset with people wearing variety of masks <br/> <br/>

2. The face mask detector was trained and the accuracy was pretty good but for some strange reasons when any person was wearing mask incorrectly, the model predicted that the person was not wearing mask at all. <br/>
I am still figuring out why that has happened but if anyone has some good modifications which can be done to improve the face mask detector please play around your way to see if you can rectify these tiny errors.
