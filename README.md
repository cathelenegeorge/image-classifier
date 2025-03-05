# image-classifier
Building a simple CNN image classifier to recognise handwritten digits using MNIST data set that consist of 28 by 28 grayscale handwritten images of numbers from 0 to 9. 
Steps to implement:

1.Install required libraries such as numpy, keras and tensorflow

2.Load the MNIST dataset

3.Preprocess the data

   3.1 Normalisation :  Divide training and testing images by 255 to scale them as values between 0 and 1, hence making the training more faster and stable

  3.2 Reshaping : CNN expects each image in 3D shape(height ,width, channels),since MNIST is grayscale it has only 1 channel

 3.3 One hot coding : Done for multi class classification done with the help of"to_categorical" function

4.Build the model:

Implement about 3 convolutional layers(Conv2D,MaxPooling) each consisting of a number of neurons and let the dimension be 3 * 3,activation function is RELU,Additionally flatten the 3D output to 1D output and finally add a dense layer.Construct an output layer which is dense with activation function as Softmax.Compile the model using Adam optimiser, loss as categorical cross entropy and metrics is accuracy

5.Train the model:

fit the model using training images and its labels, take epochs as 5 and batch size as 64,use the test data as validation data

6.Evaluate and making predictions:

can be done with the help of ".evaluate" function
