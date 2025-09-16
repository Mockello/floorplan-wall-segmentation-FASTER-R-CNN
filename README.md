# floorplan-wall-segmentation-FASTER-R-CNN
" Faster R-CNN model for wall detection in floorplan images using Detectron 2 "

This project focuses on detecting wall structures in architectural floorplans using Faster R-CNN implemented via Detectron2. The goal is to automate structural element recognition to support digital workflows in real estate, interior design, and construction.

📌 Project Objective
Architectural floorplans contain critical spatial information, but manual interpretation is time-consuming and error-prone. This project builds a robust object detection pipeline to identify walls from floorplan images, enabling:
- Faster digital processing of architectural layouts
- Improved accuracy in structural interpretation
- Scalable integration into downstream design or planning tools

🧩 Core Workflow
- Data Preparation
- Floorplan images annotated in COCO format
- Focused on wall regions with bounding boxes and category IDs
- Model Training
- Trained a Faster R-CNN model using Detectron2
- Leveraged GPU acceleration via Google Colab
- Tuned hyperparameters for domain-specific performance
- Inference & Visualization
- Ran predictions on unseen test images
- Visualized bounding boxes over wall regions
- Saved outputs for qualitative review
- Evaluation
- Measured performance using COCO metrics
- Focused on Average Precision (AP) for wall detection
- Validated consistency across varied floorplan styles

🏗 Tech Stack

Framework: Detectron2

Language: Python 3.11

Libraries: PyTorch, OpenCV, Matplotlib, pycocotools

Environment: Google Colab (GPU-accelerated training)



📊 Results
- The trained model demonstrates high accuracy in detecting wall structures
- Visual outputs show precise bounding boxes aligned with architectural features
- Evaluation metrics confirm robust generalization across test samples

🔑 Key Learnings
- How to prepare a custom COCO dataset for architectural analysis
- Training object detection models on non-natural image domains
- Using COCO AP metrics to evaluate structural detection
- Building an end-to-end pipeline from annotation to inference

📁 Repository Contents
wall-segmentation-model/
├── model.py              # Defines Faster R-CNN architecture
├── train.py              # Training loop and dataset registration
├── inference.py          # Prediction and visualization script
├── requirements.txt      # Dependencies for setup
├── results/              # Sample output images with wall detections
└── README.md             # Project overview and usage guide



Getting Started
pip install -r requirements.txt


Training:
python train.py --data_dir path/to/train_data --epochs 50


Inference:
python inference.py --input path/to/image.png --output results/output.png


