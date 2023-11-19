# Neural Network to Recognize Handwritten Digits with TensorFlow

I used Tensorflow in order to recognize the handwritten digits from 0 to 9 by training a
neural network. We build and trained the neural network that will be able to classify our own
handwritten digits with high accuracy.

# Loading the data:

We are going to use the so called MNIST dataset of handwritten digits. It has a training set of
60,000 images and a test set of 10,000 images. These images have a resolution of 28x28 pixels.
We directly imported it from Tensorflow.

# Normalize the data:

After loading the data, I normalized the training and testing data from 0 to 1.i am only
normalizing the x-values since the y values needs to stay the way they are (digits from 0 to 9).

# Building the Neural Network:

After loading and normalize the dataset, I build the neural network .For this I use tensorflow and simply define my model architecture and individual layers.For this,I use Sequential model. This is a linear type of neural network which is defined layer by layer.This is a default model.First layer is flatten layer and this type of layer flattens the input. As input shape is 28x28 and flatten transformed this shape into on dimension which would here is 784x1. After this I add two dense layers which is our hidden layers. I choose two layers with 128 neurons each. The activation function I used is relu. The output layer is also a dense layer and it has 10 neurons because of possible digits (0-9).

# Training and Testing:

By passing the training data, model will recognize the relationship between the pixels(xvalues) and the digits (y-values). There are 60,000 training examples. The epochs define how many times we are going to feed the same data so it can adjusts its parameter every time and get more and more accurate. For testing we are only interested in two values – the loss and accuracy.

# Graph and results:

We made a confusion matrix to see how many times we get correct answer and how many
times our prediction goes wrong.

For example:
As you can see 0 is predicted 974 times correctly. Six times the input was zero but our model
predicted wrong so six times it’s false negative .Fifty Eight times input digit was different but
our model predicted it’s 0 digit so false positive are 58.

 ![Capture](https://github.com/UmerrAhsan/RecognizingHandWrittenDigits/assets/102358591/4d72bbb7-739a-4f17-9cd2-4ea77ca3e02c)

