# DeepLearning_DeepCNN_Lib
This Repo is a open source DeepCNN library built by Professor Jeremy Watt, and Bowen. The API will be published recently, and there are some good experiments on toy dataset: MNIST and Cifar-10.

## DeepCNN API

Note in terms of usage, there are now 7 steps to setting up a convnet using our api

1) **Setting up the experiment via** `Setup` - here we load in the data, normalize it using a standard or ZCA-sphereing.


2) **Constructing the convnet portion of the network ** - this involves adding `conv`, `pool`, and `activation` layers.  Note when adding a conv layer via `add_conv_layer` you can turn on / off padding by setting `pad = True` or `pad = False` (note: the default is `pad = True`), control the convolution stride via the `stride` variable, `num_kernels` and `kernel_size` directly.  You can likewise control the pooling stride via the `stride` variable when adding a pooling layer via `add_pool_layer`.


3)  **Constructing the fully connected portion of the network** - You can set any number perceptron in each fully connected layers.


4)  **Choosing a cost function** - Select cost function for different problem you are solving: Regression, two-classification or multiclassification


5)  **Running an optimization** - Set the hyperparameters, notice: the each iteration means running the whole train dataset once.

6) **Saving the training result** - You can save the tuned model and reload it in next time.

7) **Make prediction based on a tuned model** - Load the tuned weights, and make prediction.

## Training on 10000 MNIST image dataset
#### Model: 
####        One layer CNN : 8 kernels ; (3,3) kernel size 
####        Pooling layer : stride = 2
####        Activation: Relu
####        Fully connected layer: 10

#### Training result
Notice: Here we only use 5 iterations 
<img width="1431" alt="2018-05-12 5 56 25" src="https://user-images.githubusercontent.com/36088488/39962295-095fe6ce-5610-11e8-97bd-a68af9b5617c.png">

### Example predictions on MNIST Test set
<img width="1200" alt="2018-05-12 6 10 50" src="https://user-images.githubusercontent.com/36088488/39962294-fa809fea-560f-11e8-9c12-b4421881a36b.png">
