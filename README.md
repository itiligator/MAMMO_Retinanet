# Detection of masses in mammograms using a one-stage object detector based on a deep convolutional neural network
Hwejin Jung, Bumsoo Kim, Inyeop Lee, Minhwan Yoo, Junhyun Lee, Sooyoun Ham, Okhee Woo, and Jaewoo kang 
Submitted in [Plos One](http://journals.plos.org/plosone/) 

## Introduction
Several computer aided diagnosis (CAD) systems have been developed for mammography; however, they are not yet widely employed for clinical use due to their inconsistent performance, which can be attributed to their reliance on hand-crafted features. Hand-crafted features are difficult to apply on mammogram images that vary due to factors such as the breast density of patients and differences in imaging devices. To address these problems, several attempts have been made to leverage a deep convolutional neural network that does not require hand-crafted features. Among the recent object detectors, RetinaNet is particularly promising as it is a simpler one-stage object detector that is fast and efficient while achieving state-of-the-art performance. RetinaNet has been proven to perform conventional object detection tasks but has not been tested on detecting masses in mammograms. Thus, we propose a mass detection model based on RetinaNet. To validate its performance in diverse use cases, we construct several experimental setups using the public dataset INbreast and the in-house dataset GURO. In addition to the conventional evaluation method of training and testing the same dataset (e.g., training and testing on INbreast), we evaluate our mass detection model on setups using additional training data (e.g., training on INbreast + GURO and testing on INbreast). And we also evaluate our model on setups using pre-trained weights (e.g., using weights pre-trained on GURO, training and testing on INbreast). In all the experiments, our mass detection model achieves comparable or better performance than more complex state-of-the-art models including the two-stage object detector. Also, the results show that fine-tuning the model using the weights pre-trained on datasets achieves similar performance improvements as using datasets directly in training phase. Therefore, we make our mass detection model's weights pre-trained on both GURO and INbreast publicly available. We expect that researchers who train RetinaNet on their in-house dataset for the mass detection task can use our pre-trained weights to leverage the features extracted from the datasets.  


## Requirments

This code has been tested on Ubuntu 16.04 64-bit system.

### Prerequisites

[Python 2](https://www.python.org/download/releases/2.7.2/)

[Keras](https://keras.io/)

[TensorFlow](https://www.tensorflow.org/)

[INbreast mammography dataset](http://medicalresearch.inescporto.pt/breastresearch/index.php/Get_INbreast_Database) 


## Installation

1. Clone this repository.
2. In the repository, execute pip install 



## Usage
### Train

Use the python code for train

    $ keras_retinanet/bin/train.py csv <train_list.csv> <ClassLable.csv> <DataType>
    
or use shell scripts code.

    $ sh train.sh   
<!--

    $ keras_retinanet/bin/train.py csv '/media/hwejin/SSD_1/DATA/DATAForPaper_v2/GURO/0_train.csv' '/media/hwejin/SSD_1/DATA/DATAForPaper_v2/Common/class.csv' 'GURO'
-->
    
### Test

Use the IPython notebook code for test.

     test.ipynb

## Pretrained Weights

Weights pretrained on GURO and INBreast are availabel at [Download Available Link](https://drive.google.com/open?id=12H5E07s3m3pcDtqDpDmWs0IpWt6CIUrb).

### Using pre-trained weight
Set the arg 'weight' to 'INBreast' or 'GURO'.

    $ keras_retinanet/bin/train.py --weight 'DataType' csv <train_list.csv> <ClassLable.csv> <DataType>
    
    
    
    


## Contact

Hwejin Jung(hwejin23@gmail.com)



## Acknowledgements

Our code is inspired by the [Keras RetinaNet](https://github.com/fizyr/keras-retinanet)
