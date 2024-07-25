# Hierarchical Multi-Label Object Detection to Analyze Panoramic Dental X-rays

DH 602: Machine Learning and Statistical Methods for Healthcare
-
The images go through 3 stages: 
1. Detection of Quadrants
2. Detection of Individual Teeth
3. Classification of Teeth into the disease categories

The project also adds wavelet compression on the images to help improve compute times. The code for this is in the Wavelet_Compression.ipynb notebook

Folder description:
-
Detection: Contains the detection models, both of which use [Co-DETR](https://github.com/Sense-X/Co-DETR) from the [MMDetection](https://github.com/open-mmlab/mmdetection) library.

  Model files are in Co-DETR/projects/configs/dental/

  Experiment logs are stored in Co-DETR/experiments/
  
  Use command
  ```bash
  bash tools/dist_train.sh <path-to-python-model-file> <number-of-gpus-to-use> <path-directory-to-store-output>
  ```
  for training the models
  
  The outputs consist of .pth files of the best epochs encountered during training and the training logs.

Classification: Contains classifier models (EfficientNet) enhanced by wavelet features. Also contains the code for long-tailed problem solutions (focal loss, intelligent subset selection, geometric augmentation).

Project Team: Amruta Parulekar, Annie D'Souza, Sanjhi Priya, Bhavya Singh, Bhavya Kohli, Tejaswee Sulekh
