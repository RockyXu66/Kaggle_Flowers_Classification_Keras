# Kaggle_Flowers_Classification_Keras

### Descrition
This is my practice for deep learning. The dataset is from Kaggle's [Flowers Recognition](https://www.kaggle.com/alxmamaev/flowers-recognition). The goal is to classify five kinds of flowers (chamomile, tulip, rose, sunflower, dandelion) by raw image.

### Dataset
The dataset contains 4242 images of flowers. The pictures are divided into five classes: chamomile, tulip, rose, sunflower, dandelion. For each class there are about 800 photos. Photos are not high resolution, about 320x240 pixels.

### Preprocessing
1. Resize all the input images to 224x224.
2. 0.8 training samples && 0.2 validation samples

### Model
There are three kinds of network architectures I used for this dataset.
1. The first model is build from scratch which has four layers.
2. The second model is build by pre-trained model VGG19 (freezing first 5 layers && include_top=False) and customed fully connected layer.
3. The third model is build by pre-trained model ResNet-50 ((freezing the first layer && include_top=False) and customed fully connected layer.

### Result
| Model | Accuracy for validation samples |
| :-: | :-: |
| Built from scratch | 0.72 |
| Built by VGG19 | 0.4 |
| Built by ResNet-50 | 0.92 |
