# YOLO_version1
This is the python3 script for object detection with YOLO version1 system, and this program is runned in [Google Colabotory](https://colab.research.google.com).

# Build environment
The environment structure showed below.
```
+ data
|
|___ 
|   + pascal_voc
|   |
|   |___ + output
|   |
|   |___ + VOCdevkit
|        |
|        |___ + Dataset(eg.VOC2007)
|___ 
|   + weights
|   |
|   |___ + YOLO_small.tar.gz
|   
+ utils
|
|___ + python scripts
|
+ yolo
|
|___ + python scripts
|
+ train.py & test.py & result.png
```

Firstly, please connect your [Google Drive](https://drive.google.com) to Google Colabotory. You can type this code in your Colabotory.

> from google.colab import drive  
drive.mount('/content/drive/')

Next you need to git this repository into your Google Drive.

> %cd drive/My\ Drive  
!git clone https://github.com/thompsonhu/YOLO_version1.git

Then download the PASCAL VOC 2007 data set.

> %cd data  
!wget http://pjreddie.com/media/files/VOCtrainval_06-Nov-2007.tar  
!tar xf VOCtrainval_06-Nov-2007.tar

Finally you also need to download the weight file into your Google Drive. Uncompress this file by using command:

> %cd weights  
!tar zxf YOLO_small.tar.gz  
!ls

# How to train the data?
Run the script by using command:

> !python3 train.py

# How to test the model?
Run the script by using command:

> !python3 test.py

# Detection Result
After training the model like the orginal paper described, we can get the detection result.

![](result.png)

# Reference
1.[hizhangp.yolo_tensorflow](https://github.com/hizhangp/yolo_tensorflow)  
2.[YOLO:Real-Time Object Detection](https://pjreddie.com/darknet/yolo/)  
3.[Pascal VOC Dataset Mirror](https://pjreddie.com/projects/pascal-voc-dataset-mirror/)