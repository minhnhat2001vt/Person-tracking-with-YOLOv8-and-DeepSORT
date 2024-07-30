# Person Tracking with YOLOv8 and DeepSORT


Object Tracking is an important problem in the field of Computer Vision, requiring the ability to continuously track and determine the location of objects in continuous video frames. One of the popular methods to solve this problem is to use a combination of the YOLOv8 model and the DeepSORT algorithm.

The goal of this project is to build a Person Tracking model that can takes an video containing people as input, then returns the trajectory of the peole in video as outputs.
## 1. Dataset
- The dataset using in this project is MOT17, which is a dataset for Multiple Object Tracking problem.
- Contains 507 natural scene images, (including 258 training images and 249 test images) in total.
- Dataset download at: https://motchallenge.net/data/MOT17/
## 2. Data Preparation
- Label processing for images folder and normalize bounding box to match YOLOv8 format.
- Arrange folders for training.
## 3. Object detection with YOLOv8
- Model summary: 168 layers, 11125971 parameters, 0 gradients, 28.4 GFLOPs
- Training: train with 50 epochs
- Evaluation: 0.453 mAP50, 0.323 mAP50-95, 0.779 R
## 4. Object Tracking with DeepSORT
- Deep Learning-Based Feature Encoding: Uses a neural network model to extract features from objects.
- Cosine Distance Metric: Measures similarity between feature vectors to match objects across frames.
- Efficient Object Tracking: Maintains and updates tracks of multiple objects using appearance and motion information.

## 5. References
- Ultralytics. (2023). YOLOv8: Real-Time Object Detection. Retrieved from https://github.com/ultralytics/yolov8.
- Wojke, Nicolai, Bewley, Alex, and Paulus, Dietrich. Simple online and realtime tracking with a deep association metric. Proceedings of the IEEE International Conference on Image Processing (ICIP), 2017, pages 3645-3649.

 
