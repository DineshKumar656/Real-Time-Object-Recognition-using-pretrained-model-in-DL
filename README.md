# Real-Time Object Detection with OpenCV and MobileNet-SSD

This Python script uses OpenCV and a pre-trained MobileNet-SSD (Single Shot Detector) model to perform real-time object detection from a webcam feed. It identifies 21 common objects and draws a bounding box with a confidence label around them.

(Suggestion: Add a screenshot or GIF of your script running here!)

Features
Real-time detection from your default webcam.

Lightweight Model: Uses MobileNet-SSD, which is fast and designed for mobile/embedded devices.

21 Object Classes: Trained to recognize the following objects:

background, aeroplane, bicycle, bird, boat, bottle, bus, car, cat, chair, cow, diningtable, dog, horse, motorbike, person, pottedplant, sheep, sofa, train, tvmonitor, mobile

Configurable Confidence: Easily adjust the confThresh variable to filter out weak detections.

Requirements
Python 3.x

OpenCV

NumPy

imutils

Installation
Clone this repository (or download the files):

Bash

git clone [YOUR_REPOSITORY_URL]
cd [YOUR_REPOSITORY_FOLDER]
Install the required Python libraries: It's recommended to create a requirements.txt file with the following content:

numpy
opencv-python
imutils
Then, install them using pip:

Bash

pip install -r requirements.txt
Download the Pre-trained Model Files: This script requires two files to run the MobileNet-SSD model. You must download them and place them in the same folder as your Python script.

1. The Prototxt (Architecture) File:

File: MobileNetSSD_deploy.prototxt.txt

Download from: github.com/chuanqi305/MobileNet-SSD

(Click "Raw" and then save the page as MobileNetSSD_deploy.prototxt.txt)

2. The Caffe Model (Weights) File:

File: MobileNetSSD_deploy.caffemodel

Download from: Google Drive Link (from the official repo)

(Download this file and save it as MobileNetSSD_deploy.caffemodel)

After this step, your folder should look like this:

.
├── your_script_name.py
├── MobileNetSSD_deploy.prototxt.txt
├── MobileNetSSD_deploy.caffemodel
└── (optional) requirements.txt
Usage
Once all requirements are installed and the model files are in the same directory, run the script from your terminal:

Bash

python your_script_name.py
A window titled "Frame" will open, showing your webcam feed.

The script will begin drawing boxes around any detected objects.

Press the Esc key to quit the program.

Configuration
You can easily tweak the script's behavior by changing these variables at the top of the file:

confThresh = 0.2: This is the minimum confidence threshold. It's set to 0.2 (or 20%). Raise this value (e.g., to 0.5) to display only detections that the model is more certain about. This will reduce false positives but might miss some real objects.

CLASSES: This list maps the model's output index to a human-readable name. You can see all the objects the model can detect here.

vs = cv2.VideoCapture(0): The 0 means it will use your default webcam. If you have multiple cameras, you can try 1, 2, etc.
demo:
<img width="1916" height="1074" alt="Screenshot 2025-10-22 082953" src="https://github.com/user-attachments/assets/779f61da-f0cf-4290-bc0e-d891d32a0826" />
<img width="1886" height="1059" alt="Screenshot 2025-10-22 083050" src="https://github.com/user-attachments/assets/3185e032-b62a-4e21-b28f-24c33fcaffa0" />
<img width="1852" height="1057" alt="Screenshot 2025-10-22 083110" src="https://github.com/user-attachments/assets/a8c81f1f-db8e-47e5-8612-46311e096722" />
<img width="1788" height="1079" alt="Screenshot 2025-10-22 083138" src="https://github.com/user-attachments/assets/41e17fdf-9864-43d3-8414-fd7793379c2b" />
<img width="1768" height="1079" alt="Screenshot 2025-10-22 083642" src="https://github.com/user-attachments/assets/c974f4db-a134-48fe-a705-445640a1f748" />
<img width="1779" height="1051" alt="Screenshot 2025-10-22 083925" src="https://github.com/user-attachments/assets/5b8eaa62-89f3-4e87-9e38-a15301a56081" />
<img width="1796" height="1029" alt="Screenshot 2025-10-22 083658" src="https://github.com/user-attachments/assets/b23f6d46-222c-4f94-b5a0-144c9ef5e479" />
<img width="1787" height="1046" alt="Screenshot 2025-10-22 083905" src="https://github.com/user-attachments/assets/e814a6fd-edf9-453b-a806-6f0bddf292b4" />







