

# Pedestrian Vehicle Detection

Training data: BDD100K
Classes of number：13   ['person','rider','car','bus','truck','bike','motor','tl_green','tl_red','tl_yellow','tl_none','traffic sign','train']

```bash
pip install -r requirements.txt

python train.py --data autodrive_data.yaml --cfg autodrive.yaml --batch-size 32

python train.py --resume ./runs/train/exp/weights/last.pt
```

```bash
python detect.py --weights ./runs/train/exp/weights/best.pt --source ./BDD100K/images/test --conf 0.3

python detect.py --weights ./runs/train/exp/weights/best.pt --source ./BDD100K/images/vedio/new/*.mp4 --conf 0.3

python test.py --data autodrive_data.yaml --weights ./runs/train/exp/weights/best.pt
```







