# Summer_Project_IIITB
## Part-1 Live Object Detection using webcam
### Overview
This project utilizes the ssd_mobilenet_v2_coco_2018_03_29 model for real-time object detection through a webcam. The Single Shot Multibox Detector (SSD) with MobileNet V2 is optimized for fast and efficient object detection, making it well-suited for live applications on resource-constrained devices.
All the project files can be downloaded from the following link below

https://iiitbac-my.sharepoint.com/:u:/g/personal/divyam_satle_iiitb_ac_in/EeiHcSRtUAtAkw8whEl9DYEBxJsALcxWC7NjyOtw7jjklQ?email=kurian.polachan%40iiitb.ac.in&e=0MTJzK

The primary steps involved include loading a pre-trained TensorFlow Lite model, running the model inference on video frames, and visualizing detection results in real time.

### Algorithm Explanation: SSD with MobileNet V2
Single Shot Multibox Detector (SSD): SSD is an object detection framework that detects objects in an image in a single pass, or "shot." It divides the image into a grid and predicts bounding boxes and classes directly within each grid cell.

MobileNet V2 Backbone: The MobileNet V2 is a lightweight neural network designed for mobile and edge devices. It reduces computation while maintaining accuracy through depth-wise separable convolutions.

Object Detection Pipeline: The SSD model predicts multiple bounding boxes with confidence scores for each object. The boxes are then filtered based on a confidence threshold (here, set to 0.5) to remove low-confidence predictions.

### Project Components and Code Structure

Model and Label Map Loading

Model Loading: The TensorFlow model is loaded from a frozen graph (frozen_inference_graph.pb) using tf.GraphDef.

Label Map Loading: The label map file (mscoco_label_map.pbtxt) maps class IDs to human-readable names, such as "person" and "car."

Inference and Object Detection

Running Inference: The run_inference_for_single_image() function processes each frame by expanding dimensions (to match model input), running it through the model, and returning detection results (bounding boxes, scores, classes).

Bounding Boxes and Class Labels: For each detection, if the confidence score exceeds 0.5, the bounding box and label are drawn on the frame.

Real-time Processing

The cv2.VideoCapture(0) function opens the webcam feed, processes frames continuously, and displays detection results in real-time.

### Code Walkthrough

Model and Label Map Loading

![image](https://github.com/user-attachments/assets/9f8e3099-3bc9-4312-a3e9-e9d6ab66a932)








