# Facial Recognition for User Authentication
Authors: Andrew Catoiu, RJ Livelo

<br>
<br>

## About This Project
<strong>Goal</strong><br>
In this project, we gathered images of faces. Some were of our own, and the rest were of random faces on the internet. Our goal is to authenticate device users my detecting their face on the computer webcam using Roboflow and OpenCV.<br>

<strong>Roboflow</strong><br>
We trained a Roboflow model using various images as our dataset. First, create a new project inside of a Roboflow workspace. Next, upload a folder of images to the working dataset. You can test this on your own by downloading the ./faces in our repository. Since we are doing facial recognition to authenticate a specific user, we will annotate the images of the user's face by labeling with their name. The non-user face images can be labeled as "Other", "Unauthorized", etc. So if the valid user of our program is RJ, the images of RJ's face should be labeled with his name. Additionally, if we want Andrew to be another valid user, then we would label his images by his name as well.
<br>
Train the model and wait 10-15 minutes for the email confirmation. After receiving the email, navigate to the "Hosted Image Inference" deployment wihtin the "Deployments" tab. Here, you obtain your API key (in the code snippet) and the project name (example: 'test-z8tjn') in the model dropdown menu.
<br>

<strong>YOLOv8</strong><br>
After training, we obtained the deployment information (API key, version number, and project name) so that we can pass them as function arguments into the online YOLOv8 colab notebook:<br>
https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb#scrollTo=BSd93ZJzZZKt
<br><br>
Follow instructions and run all the commands in the colab notebook to download a trained model of the images. When you get to "Step 5: Exporting dataset", make sure to pass the deployment information you obtained into the functions into the kernel. After running all commands, locate the custom model file in the {HOME}/runs/detect/train/weights path within the colab file manager. The model file name should be weights/best.pt, you can now download that file to your local machine.
<br>

<strong>OpenCV</strong><br>
Copy the path to the custom model file that you downloaded. Open test.py. To initialize our custom model to our program, pass the path of the file as a YOLO function argument.

<br>
<br>

## Necessary dependencies/libraries
Roboflow:
```
pip install roboflow
```

OpenCV:
```
pip install opencv-python
```

Ultralytics:
```
pip install ultralytics
```
<br>

## Testing
To test our object detection program, run the following in the correct directory:

```bash
python test.py
```

You can press <strong>q</strong> to quit the program.