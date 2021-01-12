# Star Sensor Algorithms Runnable
This repository is for running the training files under a linux virtual server. Before running the files, the dependencies must be installed.

## Dependencies
1. Install Python 3.6.2
2. Install the required libraries:
    * Numpy
    ```bash
    pip install numpy
    ```
    * Imutils
    ```bash
    pip install imutils
    ```
    * Matplotlib
    ```bash
    pip install matplotlib
    ```
    * OpenCV
    ```bash
    pip install opencv-python
    ```
    * Tensorflow
    ```bash
    pip install tensorflow
    ```

## Running Python Files
Go ahead inside the directory:
```conv-net_initial-results/raw_train/```
Run the following files in this order:

1. ```generating_data.py```  
<br>In this point you will generate the initial images to be trained. In line 14 of the code you need to change it accordingly to the path in your local machine directing to: ```conv-net_initial-results/stellarium_images/```.
2. ```data_preprocessing.py```
<br>This file will generate the image variations that will be used to train and test the data. After running this file, the folder ```conv-net_initial-results/raw_train/dataset/train/``` will be filled with the image variations.
3. ```train_test_split.py```
<br>This script will split the dataset in the training folder to a specified ratio of test/train to the test and train folder in the dataset.
4. ```train.py```
<br>This is where the training takes place, it may take a while but hold on to it. After running this script, the neural network model will be saved as ```raw_train_model.h5```.
5. ```evaluate.py```
<br>This script tests the accuracy of the model by predicting the classes inside the testing dataset.
