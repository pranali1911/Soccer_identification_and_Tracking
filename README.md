# Soccer_identification_and_Tracking

 Soccer Identification and Tracking
This project focuses on detecting and re-identifying soccer players and the ball across different camera views using advanced computer vision techniques. It leverages YOLOv11 for object detection and includes a custom tracking and re-identification pipeline.

# 📌 Project Objectives

* **Player & Ball Detection:**
  Use **YOLOv11** to accurately detect **players and the ball** in each frame of soccer videos. This forms the foundation for further tracking and identification tasks.

* **Re-identification:**
  Match and **re-identify players across different camera views**, such as the broadcast and tacticam angles, ensuring each player is recognized consistently even when the viewpoint changes.

* **Tracking:**
  Assign and maintain **consistent player IDs over time**, enabling reliable **player tracking both within a single camera view and across multiple camera angles** throughout the match.

# 📂 Dataset Annotation
 **Classes:**
* **player -** team player

* **ball –** For tracking the soccer ball.

* **Annotation Tool:** Roboflow

* **Format:** YOLO format with bounding box coordinates and class labels.

# 🧠 Technologies Used
* ## Category	Tools/Frameworks 

   Detection	YOLOv11 (Ultralytics)

   Annotation	Roboflow

   Language	Python

   Deployment	ONNX (for model export)

   Visualization	OpenCV, Matplotlib

## Model Training

from ultralytics import YOLO

model = YOLO("yolo11n.pt")
results = model.train(data="data.yaml", epochs=100)

## Export Model
model.export(format="onnx")

# Re-Identification & Tracking Pipeline
Player Detection: Run YOLOv11 on both camera feeds.

Feature Extraction: Extract embeddings or appearance-based features.

Cross-Camera Matching: Match players across camera views using cosine similarity or tracking algorithms like DeepSORT or OC-SORT.

Tracking: Assign consistent IDs using tracking-by-detection.

# OUTPUT:

![output_image_with_detections](https://github.com/user-attachments/assets/1ca0022d-ebc0-4a9e-8f56-25a701a1df5a)

