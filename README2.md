ConfMix: Unsupervised Domain Adaptation for Object Detection via Confidence-based Mixing

Installation:(We recommend the use of a Linux machine equipped with CUDA compatible GPUs.)
To clone repo and download ckpts&necessary packages:
bash hw3_download.sh

Dataset:
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

Training/Validation: 
bash hw3_train.sh $1 $2 $3 $4
$1: directory of hw3_dataset/hw3/org/train
$2: directory of hw3_dataset/hw3/org/val
$3: directory of hw3_dataset/hw3/fog/train
$4: directory of hw3_dataset/hw3/fog/val

(you can find the best/last checkpoints, mAP curve, mAP.csv of phase1(trained on source dataset)
and phase2(trained on target dataset) respectively in the directory of 
'2023CVPDL_HW3\runs\train\cityscapes' & '2023CVPDL_HW3\runs\train\cityscapes2foggy')


Inference:
bash hw3_inference.sh $1 $2 $3 $4
$1: testing images directory that contains testing images
$2: path of output json file
$3: 0~4(0: 0%, 1: 33%, 2: 66%, 3:100%, 4: best ckpt)
