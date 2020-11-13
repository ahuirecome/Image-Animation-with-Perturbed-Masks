# Image Animation with Refined Masking

### Installation

Please install the following packages:

face_alignment            1.1.0   
ffmpeg                    4.0     
imageio                   2.8.0   
imgaug                    0.4.0   
matplotlib                3.1.3   
numpy                     1.18.1  
opencv                    3.4.2   
pandas                    1.0.3   
pillow                    7.1.2   
py-opencv                 3.4.2   
python                    3.6.10  
pytorch                   1.0.0   
pyyaml                    5.3.1   
scikit-image              0.16.2  
scikit-learn              0.22.1  
scipy                     1.4.1   
torchvision               0.2.1   

### Datasets
In order to download the datasets, follow the instructions from https://github.com/AliaksandrSiarohin/first-order-model.

### Configurations
The configuration files we use for training and evaluation, for all datasets, are located in the config folder.

### Training
In order to train for a specific dataset, run the following command:
python run.py --config config/dataset_name.yaml
Checkpoints and outputs will be saved into the log folder.

### Reconstruction
In order to evaluate video reconstruction for a specific dataset and a checkpoint path, run the following command:
python run.py --config config/dataset_name.yaml --mode reconstruction --checkpoint checkpoint_path
Outputs will be saved into the log folder.

### Animation demo
In order to run the image animation pipeline for a specific dataset and a checkpoint path, run the following command:
python run.py --config config/dataset_name.yaml --mode animate --checkpoint checkpoint_path
Outputs will be saved into the log folder.

### Repository general structure
* run.py is the entry point for all scenarios (training, video reconstruction and image animation).
* config folder contains the configuration files we use for training and evaluation, for each of the datasets.
* modules folder contains the core implementation for the networks presented in paper.
* frames_dataset.py is the dataloader we use for all datasets (train and test).
* train.py is the training code.
* reconstruction.py is the code for the video reconstruction flow.
* animate.py is the code for the image animation flow.