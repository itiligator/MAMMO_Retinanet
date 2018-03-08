# MAMMO_Retinanet
This is a repository of code for 'Mass detection in mammography using one-stage object detector based on deep convolutional neural network'.

We leverage the RetinaNet which is robust region-based deep learning model to improve the performance of mass detection. 

We made our pre-trained weights available that are trained on both the public datasets and in-house dataset so that other researchers and practitioners in the community can easily build their own high-performance mass detection model by further training our pre-trained models using their own private datasets.

# Reference Code

[Keras RetinaNet](https://github.com/fizyr/keras-retinanet)

# Installation

Follow the installation method of [Keras RetinaNet](https://github.com/fizyr/keras-retinanet)


1. Clone this repository.
2. In the repository, execute pip install . --user. Note that due to inconsistencies with how tensorflow should be installed, this package does not define a dependency on tensorflow as it will try to install that (which at least on Arch Linux results in an incorrect installation). Please make sure tensorflow is installed as per your systems requirements. Also, make sure Keras 2.1.3 or higher is installed.



# Usage
## Train
    $ keras_retinanet/bin/train.py csv <train_list.csv> <ClassLable.csv> <DataType>

    $ keras_retinanet/bin/train.py csv '/media/hwejin/SSD_1/DATA/DATAForPaper_v2/GURO/0_train.csv' '/media/hwejin/SSD_1/DATA/DATAForPaper_v2/Common/class.csv' 'GURO'
    
    $ sh train.sh
    
## Test
     $ test.ipynb

# Pretrained Weights

Pretrained Weights (GURO and INBreast) are availabel at [Download Available Link](https://drive.google.com/open?id=12H5E07s3m3pcDtqDpDmWs0IpWt6CIUrb).

Download at pretrained model at keras_retinanet/pretrainedmodel
