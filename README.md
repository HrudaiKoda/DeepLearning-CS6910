<h2>Implementation of Feedforward neural network alongside various optimizers</h2>
<p>In this implementation of neural network it consists of the following execution pipeline</p>
Weight Initialization -> FeedForward -> Loss -> BackPropagation ( weight update using optimizer ) -> Repeat for various samples 

<p>Initial Weights are either initialized using Xavier or random initializations</p>
<h2>Forward Propagation</h2>
This phase takes in input and based upon the weights per each layer and bias the activation of neurons is followed layer by layer and the respective values gets passed layer to layer until last layer where cross entropy. <br>
function is being used in current case for classification of input into available classes ( prediction ). In case of regression MSE can be used. <br>
Each layer neurons have associated activation function like sigmoid ( logistic function ), tanh , reLu <br>

<h2>BackPropogation</h2>
Based on computed loss and errors in prediction the associated weight update algorithms are invoked i.e optimizers for weight updates like gradient descent, SGD, Adam, rmsprop <br>
Accordingly the weights change based upon update rules for each layer and again the forward pass is executed with the updated weights for each layer now the forward pass is executed with another input sample and the prediction is made at last layer with the updated
weights.
This repeats for whole dataset termed as an epoch. <br>

<h2>Optimizations</h2>
There are many methodologies for optimization like weight decay, weight initializers, gradient update optimizers, batch wise updates, neurons per layer, etc <br>

The current neural network implementation is run on fashion_mnist dataset and mnist dataset and performed with an accuracy of 88% and 96.7% respectively.
