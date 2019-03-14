# 3-layer-toy-nerual-network
a vectorized NeuralNetwork with 3 layers, a input layer, a hidden layer and a output layer based on NumPy.  
  
In this NN, we implement dropout, mini batch and multiple activation functions including softmax, tanh, ReLU and sigmoid to achieve better generalization and mutable structure.  

We have implemented abundant methods in our NN.

constructor this method uses to initialize our NN, it accepts the number of nodes in the input, hidden and output layer separately, and also the activation function for the hidden and the output layer and some other arguments, such as regularize factor and drop out. Then it randomly initializes the weight matrixes for the NN.
predict This method is used to calculate the output for the given input matrix computed by the NN.
forward This method implements the forward propagation algorithm, it takes a sample input and computed the result by constantly multiplying by weight matrix and activation function.
fit This method is using the backpropagation algorithm to train the NN. It divides train data randomly into several batches, and in each batch, it calculates the gradient. It then uses the average gradient to update the weight matrixes. Additionally, if we choose to do drop out or regularization, this method will slightly change the equations a little bit. At last, it prints out the training details.
shuffle This method is reponsible for randomly divide the input data into several groups with the size of at most batch_size.
decode_output This method can decode the output of NN into useful results that human can use. It just makes the output into the class id.
calculateError This method takes the test set and calculates the loss and accuracy for the NN.
dropout_forward, dropout_backward These two methods are doing the drop out thing. One for forward and the other for backward.
