

# Pedestrian Vehicle Detection
## YOLOV5:
## Training data: BDD100K https://bdd-data.berkeley.edu/

## Classes of number：13   
['person','rider','car','bus','truck','bike','motor','tl_green','tl_red','tl_yellow','tl_none','traffic sign','train']

## Requirements
Python 3.8 or later with all [requirements.txt](https://github.com/ultralytics/yolov5/blob/master/requirements.txt) dependencies installed, including `torch>=1.7`. To install run:
```bash
pip install -r requirements.txt
```
## Training
```bash
python train.py --data autodrive_data.yaml --cfg autodrive.yaml --batch-size 32

python train.py --resume ./runs/train/exp/weights/last.pt
```
## Detecting and Testing
```bash
python detect.py --weights ./runs/train/exp/weights/best.pt --source ./BDD100K/images/test --conf 0.3

python detect.py --weights ./runs/train/exp/weights/best.pt --source ./BDD100K/images/vedio/new/*.mp4 --conf 0.3

python test.py --data autodrive_data.yaml --weights ./runs/train/exp/weights/best.pt
```
## Results
<img src="https://github.com/TtZJ2/yolov5-Pedestrian-Vehicle-Detection/blob/main/runs/detect/exp/a1.jpg" width="900">
<img src="https://github.com/TtZJ2/yolov5-Pedestrian-Vehicle-Detection/blob/main/runs/detect/exp/a2.jpg" width="900">
<img src="https://github.com/TtZJ2/yolov5-Pedestrian-Vehicle-Detection/blob/main/runs/detect/exp/a3.jpg" width="900">



