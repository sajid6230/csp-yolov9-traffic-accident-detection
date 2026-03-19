# Traffic Accident Detection from Video Footage Using a CSP-Enhanced YOLOv9 Backbone

## Overview

This repository presents a deep learning framework for detecting traffic accidents from video footage using a modified YOLOv9 architecture. The proposed approach enhances the YOLOv9 backbone by integrating Cross Stage Partial (CSP) feature partitioning and deeper ELAN-based aggregation to improve feature representation, gradient flow, and detection performance.

This repository accompanies the research paper:
"Traffic Accident Detection from Video Footage Using a CSP-Enhanced YOLOv9 Backbone"
---

## Key Contributions

* CSP-enhanced YOLOv9 backbone for improved feature extraction and gradient stability
* Deeper ELAN-based architectural modification for richer multi-branch feature aggregation
* Evaluation on a manually annotated accident dataset derived from real-world traffic videos
* Comparative analysis with YOLOv5, YOLOv8, and baseline YOLOv9 models

---

## Dataset

The dataset used in this study was derived from the Highway Incidents Detection (HWID12) dataset and manually annotated for accident detection.

Total videos: 250
Total frames: ~3000
Classes: 1 (accident)

Due to size and data-sharing limitations, the dataset is not included in this repository.

Dataset structure used in this project:

Dataset structure used in this project:

data/
  images/
    train/
    val/
    test/
  labels/
    train/
    val/
    test/

---

## Installation

Clone the repository and install dependencies:

git clone https://github.com/yourusername/yolov9-traffic-accident-detection.git
cd yolov9-traffic-accident-detection
pip install -r requirements.txt

---

## Training

Run the training script:

python train.py

---

## Evaluation

Evaluate the trained model:

python val.py

---

## Inference

Run detection on an image or video:

python detect.py --source path/to/image_or_video

---

## Results

The CSP-enhanced YOLOv9 model achieved:

Precision: 0.601
Recall: 0.377
F1-score: 0.463
mAP50: 0.50
mAP50-95: 0.282

The proposed model outperforms YOLOv5, YOLOv8, and baseline YOLOv9 under the same experimental conditions.

---

## Reproducibility

This repository provides:

* Training and evaluation scripts
* Configuration files (YAML)
* Model implementation details
* Experimental setup information

All experiments were conducted using consistent training settings and evaluation protocols as described in the paper.

---

## Project Structure

models/
scripts/
utils/
tools/
segment/
panoptic/
classify/
figures/
data/ (structure only, no dataset included)
train.py
val.py
detect.py
requirements.txt
README.md
.gitignore

---

## Notes

* Model weights (.pt files) are not included due to size limitations.
* Dataset is not included due to sharing restrictions.
* The repository focuses on reproducibility of methodology and experiments.

---

## Citation

If you use this work, please cite:

@misc{ahmed2026accident,
  title={Traffic Accident Detection from Video Footage Using a CSP-Enhanced YOLOv9 Backbone},
  author={Ahmed, Sajid and Tabassum, Tasnia and Das, Madhab Chandra and Hussain, Uzair and Pham, Vung},
  year={2026},
  note={Manuscript under review}
}

---

## Acknowledgment

This work builds upon the YOLOv9 framework and related open-source contributions.
