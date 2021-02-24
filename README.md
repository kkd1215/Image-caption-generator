# Image Caption Generator

In this project, we will be implementing the caption generator using CNN (Convolutional Neural Networks) and LSTM (Long short term memory). The image features will be extracted from Xception which is a CNN model trained on the imagenet dataset and then we feed the features into the LSTM model which will be responsible for generating the image captions.

# The Dataset

For the image caption generator, we will be using the Flickr_8K dataset. There are also other big datasets like Flickr_30K and MSCOCO dataset but it can take weeks just to train the network so we will be using a small Flickr8k dataset. The advantage of a huge dataset is that we can build better models.

It can be downloaded from [Kaggle](https://www.kaggle.com/adityajn105/flickr8k)

__Flicker8k_Dataset__ – Dataset folder which contains 8091 images.

__Flickr_8k_text__ – Dataset folder which contains text files and captions of images.

# Libraries 

This project requires good knowledge of Deep learning, Python, working on Jupyter notebooks, Keras library, Numpy, and Natural language processing.

Make sure you have installed all the following necessary libraries:

  - tensorflow
  - keras
  - pillow
  - numpy
  - tqdm

# What is CNN?

Convolutional Neural networks are specialized deep neural networks which can process the data that has input shape like a 2D matrix. Images are easily represented as a 2D matrix and CNN is very useful in working with images.

CNN is basically used for image classifications and identifying if an image is a bird, a plane or Superman, etc.

# What is LSTM?

LSTM stands for Long short term memory, they are a type of RNN (recurrent neural network) which is well suited for sequence prediction problems. Based on the previous text, we can predict what the next word will be. It has proven itself effective from the traditional RNN by overcoming the limitations of RNN which had short term memory. LSTM can carry out relevant information throughout the processing of inputs and with a forget gate, it discards non-relevant information.

# Model

So, to make our image caption generator model, we will be merging these architectures. It is also called a __CNN-RNN model__.

CNN is used for extracting features from the image. We will use the pre-trained model Xception.
LSTM will use the information from CNN to help generate a description of the image.
