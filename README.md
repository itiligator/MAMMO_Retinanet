# MAMMO_Retinanet


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
