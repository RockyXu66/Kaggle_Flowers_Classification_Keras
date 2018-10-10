# Kaggle_Flowers_Classification_Keras

### Descrition
The dataset is from Kaggle's [Flowers Recognition](https://www.kaggle.com/alxmamaev/flowers-recognition). The goal is to classify five kinds of flowers (chamomile, tulip, rose, sunflower, dandelion) by raw image.

### Dataset
The dataset contains 4242 images of flowers. The pictures are divided into five classes: chamomile, tulip, rose, sunflower, dandelion. For each class there are about 800 photos. Photos are not high resolution, about 320x240 pixels.

### Preprocessing
1. Resize all the input images to 224x224.
2. 0.8 training samples && 0.2 validation samples

### Model
There are three kinds of network architectures I used for this dataset.
1. The first model is build from scratch which has four layers.
2. The second model is build by pre-trained model [VGG19](https://keras.io/applications/#vgg19) (freezing first 5 layers && include_top=False) and customed fully connected layer.
3. The third model is build by pre-trained model [ResNet-50](https://keras.io/applications/#resnet50) ((freezing the first layer && include_top=False) and customed fully connected layer.

### Result
| Model | Accuracy for validation samples |
| :-: | :-: |
| Built from scratch | 0.72 |
| Built by VGG19 | 0.4 |
| Built by ResNet-50 | 0.92 |

### Notes
* Computing: Google Colab Tesla K80 GPU
* Python version: 3.6.3
* Using packages
  1. [`Keras`](https://www.tensorflow.org/guide/keras) (tensorflow.python.keras) for building models 
  2. [`OpenCV`](https://opencv.org/) (cv2) for processing images
  3. [`sikit-learn`](http://scikit-learn.org/stable/) (sklearn) for train_test_split 
