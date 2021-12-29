This code is a custom use of YOLO v5 from https://github.com/ultralytics/yolov5 with BDD100K dataset




Installation:
1. Download yolov5 from https://github.com/ultralytics/yolov5 
2. Transform your dataset to yolov5 format (see Dataset section below) and check the folder structure is correct 
3. Update the original files with the files from this repository
4. Run the train, detect and test as noted in Run section below







Dataset

To use YOLO v5 with your data, you need the following:
- The dataset should be in YOLO format
-   if your the objects from your dataset are marked in a different format, you have to transform it automatically using a script as: https://github.com/Delphi89/JSON2YOLOv5
-   In this project, I have added the dataset in the following structure: data/bdd100k/images and data/bdd100k/labels, in each of them the folders are train, test and val




Run


You can run from Eclipse or you can use the following commands (you have to select the right options for your custom dataset) from the project main folder:

python train.py --img 800 --batch-size 48 --epochs 100 --data bdd100k.yaml --cfg '' --weights 'yolov5s.pt'

python3 detect.py --weights weights/best5.pt

python detect.py --source 'https://www.youtube.com/watch?v=AYNT2hqs87I'
