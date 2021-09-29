# FACIAL RECOGNITION PROJECT

## Description:
There are many ways to solve the face recognition problem. In this project I will try to solve it in 2 different ways to see which is the best approach for this project.

- First approach: Using OpenCV, YOLO and Deep learning models
- Second approach: Using OpenCV, [face_recognition](https://github.com/ageitgey/face_recognition) package

## Data:
This is a teamwork project, so the data for face recognition is also our teamates:
- Tam: with 100 croped face images
- Nguyen: with 100 croped face images 
- Thu: with 100 croped face images 

## Technologies and techniques:
- [dlib](http://dlib.net/): a state-of-the-art face recognition built with deep learning. The model has an accuracy of 99.38% on the [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/) benchmark.
- face_recognition: thís package built in dlib
- tensorflow 2.6.0: I using diference of models: VGG16, EfficientNetB1, FR_MobileNetV2, ResNet50v2
- OpenCV: to manipulate webcam and frames

## Install:
- Requirements:
	- Python 3.3+
	- macOS or Linux (Windows not officially supported, but might work)
- Install Dlib: ```conda install -c conda-forge dlib```
- Install face_recognition package: ```pip3 install face_recognition```


## Result:
### First approach: Using OpenCV, YOLO and Deep learning models:
- I try to used 4 different models to see their differences: VGG16, EfficientNetB1, FR_MobileNetV2, ResNet50v2

- These deep learning models all give pretty good results, with ~100% accuracy on validation data set:

<p align="center">
  <img src="https://user-images.githubusercontent.com/87942072/135186481-ac3b8769-e675-4ede-9d23-dd2a802f2418.png" alt="Sublime's custom image"/>
</p>

- When used on a webcam, this method can classify the members' faces. However, using YOLO models to detect faces and deep learning model to make prediction in sequence makes the processing speed of the webcam very slow (lag).

<p align="center">
  <img src="https://user-images.githubusercontent.com/87942072/135188289-2093d858-3701-4c1d-b208-b24714ce94ed.png"/>
</p>

### Second approach: Using OpenCV, [face_recognition](https://github.com/ageitgey/face_recognition) package:
- With this approach, the webcam speed has increased quite a lot when compared to the above first approach
- The special thing is, we don't need too many images to train the model, each member I only take 2 images to train is enough to create a satisfy result.
- If someones not belong to the trained dataset, it will labeled it "Ai vay?" (mean "Who?")

<p align="center">
  <img src="https://user-images.githubusercontent.com/87942072/135189202-fdb92f97-2098-441e-b4c4-490832639832.jpg"/>
</p>

## Deploy app in streamlit
### Face recognition:

<p align="center">
  <img src="https://user-images.githubusercontent.com/87942072/135189620-85e58ec5-2ae5-4bcc-86ef-af28ae0dc916.png"/>
</p>

### Face make-up - nightmare! :):
<p align="center">
  <img src="https://user-images.githubusercontent.com/87942072/135189932-e8e04c4f-60e5-43c6-bec0-43caf5de9769.png"/>
</p>

### Face mask - Covid-19 mode:
<p align="center">
  <img src="https://user-images.githubusercontent.com/87942072/135190144-76ad6048-d3aa-450b-88f8-3dcb65815e7d.png"/>
</p>

## Next steps:
- Increase webcam speed by using multi-thresh techniques or reducing frame read
- Make system more stable when working in low light condition




