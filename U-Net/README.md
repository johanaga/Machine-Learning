# U-Net

**Dataset:** https://www.kaggle.com/c/carvana-image-masking-challenge/overview

**Overview:** Semantic Segmentation using U-Net architecture. Trained on Carvana dataset from Kaggle.

**Results:** Model obtains a dice coefficient of 99.2% and an accuracy of 99.7%.

**Improve:** 
 - Use metadata and create specific weights for different types of cars
 - Dialate the learning rate when val loss begins to platau
 - Add other data augmentation operations