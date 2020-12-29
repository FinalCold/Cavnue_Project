
- - -
This repository is based on yolov5.
https://github.com/ultralytics/yolov5

Some generated codes are based on convert2Yolo.
https://github.com/ssaru/convert2Yolo

- - -
# Team Cavnue

![pch](https://user-images.githubusercontent.com/69332997/103256027-03752980-49cf-11eb-9a0d-bb2c13156e7b.jpg)

ChanJong Park (박찬종)
````
* Email : cjpark137@naver.com
````

![bju](https://user-images.githubusercontent.com/69332997/103256035-096b0a80-49cf-11eb-8a51-58df5e593537.jpg)

JongWook Bae (배종욱)
````
* Email : bjonguk@gmail.com
````

![hjy](https://user-images.githubusercontent.com/69332997/103256032-07a14700-49cf-11eb-9f9f-f31eab4bfdad.jpg)

JunYeong Heo (허준영)
````
* Email : jass9869@naver.com
````
- - -
# Video

![gitvideo](https://user-images.githubusercontent.com/69332997/103191533-af0f7280-4918-11eb-859c-82f101a3ee72.gif)

- - -

## Pretrained Checkpoints

| Model | AP<sup>val</sup> | AP<sup>test</sup> | AP<sub>50</sub> | Speed<sub>GPU</sub> | FPS<sub>GPU</sub> | params | GFLOPS |
|---------- |------ |------ |------ | -------- | ------| ------  |  :------: |
| [YOLOv5s](https://github.com/ultralytics/yolov5/releases)    | 37.0     | 37.0     | 56.2     | **2.4ms** | **416** | 7.5M   | 17.5
| [YOLOv5m](https://github.com/ultralytics/yolov5/releases)    | 44.3     | 44.3     | 63.2     | 3.4ms     | 294     | 21.8M  | 52.3
| [YOLOv5l](https://github.com/ultralytics/yolov5/releases)    | 47.7     | 47.7     | 66.5     | 4.4ms     | 227     | 47.8M  | 117.2
| [YOLOv5x](https://github.com/ultralytics/yolov5/releases)    | **49.2** | **49.2** | **67.7** | 6.9ms     | 145     | 89.0M  | 221.5
| [YOLOv5x](https://github.com/ultralytics/yolov5/releases) + TTA|**50.8**| **50.8** | **68.9** | 25.5ms    | 39      | 89.0M  | 801.0

## Requirements

Python 3.8 or later with all [requirements.txt](https://github.com/ultralytics/yolov5/blob/master/requirements.txt) dependencies installed, including `torch>=1.7`. To install run:
```bash
$ pip install -r requirements.txt
```
## Preparing Dataset

You can generate VOC format(.xml) to Yolo format(.txt) with command below before you train your dataset.
```bash
$ python generate_dataset.py --img_path /path/dir --label /path/dir --volume 5
```
Then, you can get (Dataset * 1/5) amount of dataset including images and labels.
and it automatically split into train : val = 9 : 1

## Training

Training times for YOLOv5s/m/l/x are 2/4/6/8 days on a single V100 (multi-GPU times faster). Use the largest `--batch-size` your GPU allows (batch sizes shown for 16 GB devices).
```bash
$ python train.py --data nia.yaml --weights yolov5m.pt --batch-size 32 --img 640
```
<img src="https://user-images.githubusercontent.com/26833433/90222759-949d8800-ddc1-11ea-9fa1-1c97eed2b963.png" width="900">


## Inference

To run inference on example images in `data/images`:
```bash
$ python inference.py --source data/images --weights best.pt --save-xml
```

- - -
### Development Languages
````
* Python
* Cuda
````
### Development Environment
````
Ubuntu 18.04 LTS
OpenCV 4.4.0
Cuda 10.1
CuDNN 7.6.5
Python 3.8
PyTorch 1.7.1
````
### GPU
````
Nvidia Geforce Titan X 12Gb * 2
````
### Libraries
````
Yolo v5
Python
OpenCV
````

- - -
![poster](https://user-images.githubusercontent.com/67350632/103162774-0558b480-4838-11eb-9f25-a42da5ad708b.png)
