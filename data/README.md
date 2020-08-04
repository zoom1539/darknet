TRAIN:
1. copy all files in Yolo_mark\x64\Release\data to current directory
2. modify  backup = data/backup/ in obj.data
3. modify  train.txt
4. modify yolov3.cfg according AB
5. train: ./darknet detector train data/obj.data data/yolov3.cfg data/darknet53.conv.74 -gpus 0,1,2,3 -dont_show -map


TEST:
1. modify data/yolov3.cfg to test mode
2. test: ./darknet detector test data/obj.data data/yolov3.cfg data/backup/yolov3_final.weights 
3. Enter Image Path