<!--
- Title
- Banner
- Badges
- Short Description
- Long Description
- Table of Contents
- Security
- Background
- Install
- Usage
- Extra Sections
- API
- Maintainers
- Thanks
- Contributing
- License
-->

<!--Title-->

# vehicle recognition

<!-- Banner-->
<!--
<div align="center">
  <img src="images/banner.png">
</div>
-->

<!-- Badges-->
<!--
[![Python](https://img.shields.io/pypi/pyversions/tensorflow.svg?style=plastic)](https://badge.fury.io/py/tensorflow)
-->

<!-- Short or Long Description-->

YOLO v3 를 사용한 차량, 번호판 인식

<!-- Table of Contents-->

## Contents

1. [Background](#background)
1. [Install](#install)
1. [Maintainers](#maintainers)
1. [Contributing](#contributing)
1. [License](#license)

<!-- Security-->

<!-- Background-->

<!-- Install-->

## Install

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

### Dependencies

GPU : (GTX 1060 3GB), 100 epoch, 230 train

![result](./result.png)

<!-- Usage-->

<!-- Extra Sections-->

<!-- API-->

<!-- Maintainers-->

## Maintainers

[@gotoERROR00111011](https://github.com/gotoERROR00111011).

<!-- Thanks-->

<!-- Contributing-->

## Contributing

### Contributors

<img src="https://avatars.githubusercontent.com/u/20670685?s=60&v=4" />

<!-- License-->

## License

MIT License
