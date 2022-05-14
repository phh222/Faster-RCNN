# Faster-RCNN
Faster RCNN 在VOC数据集上训练并测试

# 训练步骤
数据集的准备
本文使用VOC格式进行训练，训练前需要下载好VOC07+12的数据集，解压后放在根目录

数据集的处理
运行voc_annotation.py生成根目录下的2007_train.txt和2007_val.txt。

开始网络训练
train.py的默认参数用于训练VOC数据集，直接运行train.py即可开始训练。

# 预测步骤
在frcnn.py文件里面，修改model_path和classes_path使其对应训练好的文件；model_path对应logs文件夹下面的权值文件，classes_path是model_path对应分的类。
运行predict.py，输入想要预测的图片名称和路径，如img/street.jpg.

# 评估
在frcnn.py文件里面，修改model_path和classes_path使其对应训练好的文件；model_path对应logs文件夹下面的权值文件，classes_path是model_path对应分的类。
运行get_map.py，评估结果保存在map_out文件夹中。



# Reference
https://github.com/qqwweee/keras-yolo3/
https://github.com/bubbliiiing/faster-rcnn-tf2
