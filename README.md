# vehicle recognition

## Result
Graphic Card (GTX 1060 3GB) Performance deficient    

Recommended 100 epoch, 230 train    
![result](./result.png)

## Introduction
- Vehicle license plate recognition using yolo v3

## Quick Start
- windows
    - CUDA9, cuDNN
- python=3.6
    - keras=2.1.5
    - tensorflow=1.9
    - opencv
    - matplotlib
    - pillow
    - pydot
    - graphviz

1. Data setting
    1. Download [keras-yolo3](https://github.com/qqwweee/keras-yolo3)
    1. Add ./CarPlate_dataset
    1. Run voc_annotation.py
1. Train
    1. Add ./yolov3.weights [YOLOv3-416 weights](https://pjreddie.com/darknet/yolo/)
    1. Run python convert.py yolov3.cfg yolov3.weights model_data/yolo.h5
    1. Run python train.py
    1. Move result ./logs -> ./model_data/yolo.h5
1. Run
    1. Run python yolo_video.py --image
