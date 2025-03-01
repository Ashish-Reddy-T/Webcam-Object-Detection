# Real-Time Object Detection with YOLOv3 and Webcam

This project implements real-time object detection using the YOLOv3 (You Only Look Once) model and a webcam. It detects objects in the video stream from your webcam and draws bounding boxes around them with labels and confidence scores. The project is built using Python, TensorFlow, OpenCV, and PIL (Python Imaging Library).

---

## Features

- **Real-Time Object Detection**: Detects objects in real-time using a webcam feed.
- **YOLOv3 Model**: Utilizes a pre-trained YOLOv3 model for accurate and fast object detection.
- **Bounding Boxes and Labels**: Draws bounding boxes around detected objects and labels them with their class names and confidence scores.
- **Customizable Thresholds**: Allows you to adjust the object detection threshold (`obj_thresh`) and non-maximum suppression threshold (`nms_thresh`).
- **Cross-Platform**: Works on Windows, macOS, and Linux.

---

## Requirements

To run this project, you need the following dependencies:

- Python 3.x
- TensorFlow (for loading and running the YOLOv3 model)
- OpenCV (for webcam capture and video processing)
- PIL (Python Imaging Library) for image manipulation
- NumPy (for numerical operations)

You can install the required packages using `pip`:

```
pip install tensorflow opencv-python pillow numpy
```

---

## How to Use

### 1. Clone the Repository:

```
git clone https://github.com/your-username/webcam-object-detection.git
cd webcam-object-detection
```
### 2. Download the YOLOv3 Model:

- Ensure you have the pre-trained YOLOv3 model (`YOLO_model.h5`) in the project directory. You can download it from a reliable source or train your own model.

### 3. Run the Webcam Detection:

- Execute the script to start real-time object detection:
```
python webcam_detection.py
```

### 4. Interact with the Webcam Feed:
- The webcam feed will open in a new window with bounding boxes and labels drawn around detected objects.
- Press `q` to quit the application.

---

## Code Overview

### Key Functions

- `capture_frame(cap)`:
  - Captures a frame from the webcam and converts it from BGR (OpenCV) to RGB (PIL) format.
- `detect_image(image_pil)`:
  - Performs object detection on the input image using the YOLOv3 model.
  - Returns the image with bounding boxes and labels drawn.
- `run_webcam_detection()`:
  - Opens the webcam and continuously captures frames.
  - Processes each frame using the `detect_image` function and displays the results in real-time.

### Customization

- #### Object Detection Threshold `(obj_thresh)`:
  - Adjust the confidence threshold for object detection. Default is `0.4`.
  - Example: `detect_image(image_pil, obj_thresh=0.5)`
- #### Non-Maximum Suppression Threshold (`nms_thresh`):
  - Adjust the threshold for suppressing overlapping boxes. Default is `0.45`.
  - Example: `detect_image(image_pil, nms_thresh=0.5)`

---

## Example Output

When you run the script, you will see a window displaying the webcam feed with bounding boxes and labels for detected objects. For example:

- __Person__: 0.92
- __Car__: 0.88
- __Dog__: 0.78

---

## Troubleshooting









