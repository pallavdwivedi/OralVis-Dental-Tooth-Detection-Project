# OralVis-Dental-Tooth-Detection-Project
Project Overview: Brief description of the YOLOv11-based dental tooth detection system using FDI numbering
dental-tooth-detection/
├── README.md
├── data.yaml # Dataset configuration
├── train_model.py # Training script
├── dataset_organization.py # Data preprocessing
├── evaluation.py # Model evaluation
├── requirements.txt # Dependencies
├── results/
│ ├── confusion_matrix.png # Performance metrics
│ ├── training_curves.png # Loss/mAP curves
│ └── sample_predictions/ # Test predictions
└── weights/
└── best.pt # Trained model weights


## Quick Start

### Prerequisites
pip install ultralytics opencv-python matplotlib pandas


### Training
python train_model.py



### Evaluation
python evaluation.py



### Inference
from ultralytics import YOLO
model = YOLO('weights/best.pt')
results = model.predict('path/to/dental/image.jpg')



## FDI Tooth Classification
The model detects and classifies teeth according to the international FDI numbering system:
- **Quadrants**: 1 (Upper Right), 2 (Upper Left), 3 (Lower Left), 4 (Lower Right)
- **Tooth Types**: Central Incisors, Lateral Incisors, Canines, Premolars, Molars
- **Total Classes**: 32 permanent teeth

## Key Features
- Automated tooth detection and numbering
- High accuracy FDI classification
- Real-time inference capability
- Comprehensive evaluation metrics
- Visualization of predictions with bounding boxes

## Applications
- Dental diagnosis assistance
- Automated dental charting
- Educational tools for dental students
- Dental practice management systems

## Dependencies
- Python 3.8+
- PyTorch
- Ultralytics YOLOv11
- OpenCV
- Matplotlib
- Pandas

## Acknowledgments
- Ultralytics for YOLOv11 implementation
- FDI World Dental Federation for numbering system standards
- Dataset contributors and annotators
