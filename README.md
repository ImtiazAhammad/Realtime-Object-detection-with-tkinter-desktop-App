# Realtime-Object-detection-with-tkinter-desktop-App

This project is a graphical user interface (GUI) application that utilizes YOLO v8 for object detection. It allows users to use their webcam or play video files, displaying detected objects in real-time with bounding boxes and labels.

## Features

- **Webcam Support**: Start and stop the webcam feed to perform real-time object detection.
- **Video Playback**: Select a video file to perform object detection on the video frames.
- **Class Filtering**: Filter detected objects by class using a dropdown menu.
- **Pause/Resume**: Pause or resume the video feed.
- **Quit Application**: Exit the application gracefully.

## Prerequisites

Ensure you have the following dependencies installed:

- Python 3.7+
- OpenCV
- Tkinter (usually included with Python)
- PIL (Pillow)
- Pandas
- cvzone
- ultralytics

You can install the necessary Python packages using:

```sh
pip install opencv-python-headless Pillow pandas cvzone ultralytics
```

## Setup

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/ImtiazAhammad/Realtime-Object-detection-with-tkinter-desktop-App.git
   cd Realtime-Object-detection-with-tkinter-desktop-App
   ```

2. **Prepare YOLO Model and Class File**:

   - Ensure you have the YOLOv8 model (`yolov8s.pt`) in your working directory.
   - Create a `class.txt` file with the class names (one per line) that YOLO model can detect.

3. **Prepare an Initial Image**:

   - Place an image named `photo.jpg` in your working directory to be displayed initially on the canvas.

## Usage

Run the application with:

```sh
python app.py
```

### Graphical User Interface

- **Play**: Start the webcam feed.
- **Stop**: Stop the webcam feed.
- **Select File**: Choose a video file to play and perform object detection.
- **Pause/Resume**: Pause or resume the video feed.
- **Select Class**: Filter the detected objects by selecting a class from the dropdown menu.
- **Quit**: Exit the application.

## Code Overview

Here's a brief overview of the code:

- **Imports and Global Variables**:
  - Import necessary modules and define global variables for handling the camera, frame count, model, etc.

- **Read Classes**:
  - Function to read class names from `class.txt`.

- **Webcam and Video Functions**:
  - Functions to start, stop, pause/resume the webcam or video feed.

- **Update Canvas**:
  - Function to update the Tkinter canvas with frames from the webcam or video, performing object detection and drawing bounding boxes.

- **Quit Application**:
  - Function to gracefully exit the application.

- **GUI Setup**:
  - Create the main Tkinter window and add widgets (buttons, dropdown, canvas).

- **Main Loop**:
  - Start the Tkinter main loop to run the application.


## Acknowledgements

- [Ultralytics](https://github.com/ultralytics/yolov8) for the YOLOv8 model.
- [OpenCV](https://opencv.org/) and [Pillow](https://python-pillow.org/) for image processing.
- [cvzone](https://github.com/cvzone/cvzone) for computer vision utilities.
