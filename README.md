# Soccer_identification_and_Tracking

 Soccer Identification and Tracking
This project focuses on detecting and re-identifying soccer players and the ball across different camera views using advanced computer vision techniques. It leverages YOLOv11 for object detection and includes a custom tracking and re-identification pipeline.

📌 Project Objectives
Player & Ball Detection: Use YOLOv11 to detect players and the ball in soccer video frames.

Re-identification: Match and track players across multiple camera angles (e.g., broadcast view and tacticam).

Tracking: Assign consistent IDs to players and track them over time within and across camera views.

📂 Dataset Annotation
Classes:
player - team player

ball – For tracking the soccer ball.

Annotation Tool: Roboflow

Format: YOLO format with bounding box coordinates and class labels.

🧠 Technologies Used
Category	Tools/Frameworks
Detection	YOLOv11 (Ultralytics)
Annotation	Roboflow
Language	Python
Deployment	ONNX (for model export)
Visualization	OpenCV, Matplotlib

Model Training
python
Copy
Edit
from ultralytics import YOLO

model = YOLO("yolo11n.pt")
results = model.train(data="data.yaml", epochs=100)

Export Model
python
Copy
Edit
model.export(format="onnx")

# Re-Identification & Tracking Pipeline
Player Detection: Run YOLOv11 on both camera feeds.

Feature Extraction: Extract embeddings or appearance-based features.

Cross-Camera Matching: Match players across camera views using cosine similarity or tracking algorithms like DeepSORT or OC-SORT.

Tracking: Assign consistent IDs using tracking-by-detection.

# OUTPUT:

![output_image_with_detections](https://github.com/user-attachments/assets/1ca0022d-ebc0-4a9e-8f56-25a701a1df5a)

