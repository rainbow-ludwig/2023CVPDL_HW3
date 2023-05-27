# ConfMix: Unsupervised Domain Adaptation for Object Detection via Confidence-based Mixing

## Installation
(We recommend the use of a Linux machine equipped with CUDA compatible GPUs.)
To clone the repo and download checkpoints & necessary packages, run the following command:
```bash
bash hw3_download.sh
Dataset
Please prepare the same dataset offered by TA:


Name
----
hw3_dataset
hw3_dataset/hw3/org
hw3_dataset/hw3/org/train
hw3_dataset/hw3/org/val
hw3_dataset/hw3/org/train.coco
hw3_dataset/hw3/org/val.coco
hw3_dataset/hw3/fog
hw3_dataset/hw3/fog/train
hw3_dataset/hw3/fog/val
hw3_dataset/hw3/fog/val.coco
Training/Validation
To train and validate the model, use the following command:

bash hw3_train.sh $1 $2 $3 $4
$1: Directory of hw3_dataset/hw3/org/train
$2: Directory of hw3_dataset/hw3/org/val
$3: Directory of hw3_dataset/hw3/fog/train
$4: Directory of hw3_dataset/hw3/fog/val
You can find the best/last checkpoints, mAP curve, and mAP.csv of phase 1 (trained on the source dataset) and phase 2 (trained on the target dataset) respectively in the following directories:

Phase 1: 2023CVPDL_HW3/runs/train/cityscapes
Phase 2: 2023CVPDL_HW3/runs/train/cityscapes2foggy
Inference
To perform inference, use the following command:


bash hw3_inference.sh $1 $2 $3 $4
$1: Testing images directory that contains testing images
$2: Path of the output JSON file
$3: Confidence level (0-4):
0: 0%
1: 33%
2: 66%
3: 100%
4: Best checkpoint
