# STAAB-DH602-project
# STRATEGIC TEAM ALLIANCE FOR ACHIEVING BOLD BREAKTHROUGHS


Project title: **Hierarchical Multi-Label Object Detection to Analyze Panoramic Dental X-rays**

The images go through 3 stages: 
1. Detection of Quadrants
2. Detection of Individual Teeth
3. Classification of Teeth into the disease categories

The project also adds wavelet compression to help improve compute times.

Folder description:
Detection: Contains the detection models, both of which use [Co-DETR](https://github.com/Sense-X/Co-DETR) from the [MMDetection]([url](https://github.com/open-mmlab/mmdetection)) library.
Classification: Contains classifier models (EfficientNet) enhanced by wavelet features. Also contains the code for long-tailed problem solutions (focal loss, intelligent subset selection, geometric augmentation).
