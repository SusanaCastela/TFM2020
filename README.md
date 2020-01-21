## Interpretability of Deep Learning Methods in Carotid Artery Image Classification & Semantic Segmentation

In this thesis, we explored the interpretability of Deep Learning methods applied to Medical Imagery classficiation and Segmentation. 
That is to say, the "human understandability" of the decision taken during the classification and segmentation of carotid artery ultrasound images, used to detect atherosclerosis (a know symptom of cardio-vascular disease).
\
Our results suggest that these Deep Learning methods have a solid basis to be commonly understood, and as such could be used for the automation of plaque detection and IMT calculations.

### Datsets:
* [REGICOR](https://www.regicor.org)
* Labels resulting from a previous segmentation with 2 or 6 labels

### Interpretability methods
* [SHAP values](https://github.com/slundberg/shap)
* [Grid saliency](https://arxiv.org/abs/1907.13054)

### Process
* Class assignments based on IMT values
* CNN training for regression / classification
* Carotid artery segmentation model run
* Saliency map calculation & application to segmented images

### Implementation
* The entire code was created in Python 3 and Python 2.
* For the classification of the plaque we used [Keras](https://github.com/keras-team/keras) running [Tensorflow](https://www.tensorflow.org/tutorials) on the backend. The model is a classic CNN net, either trained for classification or regression with minor changes.
* For the segmentation and grid saliency, we used both [Pytorch](https://pytorch.org/) and Keras with a [Theano](http://www.deeplearning.net/software/theano/) backend, making use of the pre-trained DeepLabV3-ResNet101 (for semantic segmentation) and VGG19 (for image classification).
* For the implementation of Tiramisu 67 we used [CarotidArtery-DomainAdaptation](https://github.com/DaniSalva/CarotidArtery-DomainAdaptation)

### Delivered on 21-01-2020 by:
* Susana Castela
* Christopher Fady
