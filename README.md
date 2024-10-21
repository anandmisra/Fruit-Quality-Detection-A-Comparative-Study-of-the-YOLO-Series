# Fruit Quality Detection: A Comparative Study of the YOLO Series
## Overview
This project is designed to automate the detection of fruit quality using computer vision techniques, specifically leveraging the YOLO (You Only Look Once) series models. Traditionally, fruit quality is determined through manual inspection, which is time-consuming and prone to errors, especially in large-scale operations. This project aims to evaluate and compare the performance of several YOLO models (YOLOv8, YOLOv9, YOLOv10, and YOLOv11) to identify the most effective model for classifying fruit quality into three categories: Fresh, Mild, and Rotten.

## Key Features
* YOLO Models Compared: YOLOv8, YOLOv9, YOLOv10, YOLOv11.
* Performance Metrics Evaluated: Precision, Recall, mAP50, and mAP50-95.
* Classes of Fruit Quality: Fresh, Mild, Rotten.
* Dataset: Fruit Quality dataset (FruitQ) with 9,421 preprocessed images.
* Real-time Detection: The models are optimized for real-time detection and localization, making them ideal for industrial applications.
## Methodology
* Data Preprocessing: Images were resized and annotated to belong to one of the three quality classes.
* Model Training: All four YOLO models were trained on the dataset, and their performance was evaluated based on speed, accuracy, and robustness.
* Comparative Study: The models were compared across various real-world conditions, including changes in lighting and fruit orientation, to determine the most suitable model for fruit quality detection.
## Results
* Best Model: YOLOv9 achieved the highest mAP50 and mAP50-95 scores (0.981 for both), along with a recall of 0.936, making it the most accurate model for detecting fruit quality.
* Other Models: YOLOv8 had a slightly higher precision (0.958) but lower recall, while YOLOv10 and YOLOv11 demonstrated strong overall performance with balanced precision and recall values.
| Model | Precision |	Recall |	mAP50 |	mAP50-95 |
| --- | --- | --- | --- | --- |
| YOLOv8 |	0.958 |	0.891 |	0.975 |	0.974 |
| YOLOv9 |	0.924 |	0.936 |	0.981 |	0.981 |
| YOLOv10 |	0.948 |	0.919 |	0.973 |	0.967 |
| YOLOv11 |	0.939 |	0.917 |	0.974 |	0.974 |

## Installation
1. Clone the repository:
```
git clone https://github.com/your-username/fruit-quality-detection-yolo.git
```
2. Install the required dependencies
```
pip install -r requirements.txt
```
## How to Run
1. Ensure your dataset is available and properly formatted.
2. Run the model training script for the desired YOLO version:
```
python train.py --model yolov9 --data ./data/FruitQ.yaml
```
3. To evaluate the model:
```
python evaluate.py --model yolov9 --data ./data/FruitQ.yaml
```

## Dataset
The dataset used is called FruitQ, which contains over 9,421 images annotated into three classes:
* Fresh
* Mild
* Rotten
Images were resized to 426x240 for efficient processing.

## Conclusion
This study identifies YOLOv9 as the best-performing model for fruit quality detection. It achieves a high level of accuracy and robustness in real-world conditions. Further research could explore enhancements in detection under occlusion and low-light conditions using advanced attention mechanisms.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgments
This project was completed as part of research work at the Vellore Institute of Technology. Special thanks to the team members and contributors: Angad Rehsi, Mayank Mishra, Anand Misra, Saranya G.

