# Gesture-Recognition
Video - classification
<p>
 The aim of this project is to  develop a cool feature for a smart-TV that can recognise five different gestures performed by the user, which will help in controlling the TV without using a remote. The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:
Thumbs up:  Increase the volume
Thumbs down: Decrease the volume
Left swipe: 'Jump' backwards 10 seconds
Right swipe: 'Jump' forward 10 seconds  
Stop: Pause the movie
 
Each video is a sequence of 30 frames (or images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use. The videos have two types of dimensions - either 360x360 or 120x160 ,depending on the webcam used to record the videos.</p>

 <p> The images in the videos were preprocessed before fed into the model. Th preprocessing steps include resizing the images and normalizing them. A custom data generator that includes the preprocessing steps was developed. The classification was done using two different approaches:
1. Convolutions + RNN
The conv2D network extracts a feature vector for each image, and a sequence of these feature vectors is then fed to an RNN-based network. Transfer learning (MobileNet) is used in the 2D CNN layer and it is folleowwed by GRU (RNN).The output of the RNN is a regular softmax with 5 outputs
2. 3D Convolutional Network, or Conv3D
 
 Since the dataset was balanced, accuracy was used for evaluating the model performance. Both the models were able to achieve a test accuracy close to 95%

