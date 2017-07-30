# Deep Convolutional Highway network - Tensorflow

The implementation of this network is based on the [Highway networks paper](https://arxiv.org/pdf/1505.00387.pdf).

The Highway Network introduces 2 gates in the normal network layer. One gate is called "Transform" gate. The Transform gate is there to control how much information is going to put through from the activation of that layer. Second gate is called the "Carry" gate. It is just *1 - Transform gate*. The Carry gate controls how much of UNMODIFIED informations we pass through the network.

By combining these two gates with normal formula for the layer **f(xW + b)** we get the next formula:

![](formula_highway_layer.png)

Note: The tricky part with DC Highway networks are dimensions. Just be conscious about the highway layer tensor dimensions.

## Install

### &nbsp;&nbsp;&nbsp; Python version
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Python version used in this project: 3.5+

### &nbsp;&nbsp;&nbsp; Dependencies

> *  [TensorFlow](http://tensorflow.org) 1.2.0
> *  [Numpy](http://www.numpy.org) 1.10.4
> *  [Time]()

### Code

The code for this project is inside **highway_dc_network.ipynb**.

### How to run

To run this project execute one of these two lines in your terminal/cmd:

`ipython notebook highway_dc_network.ipynb`

or

`jupyter notebook highway_dc_network.ipynb`


### Read more about Highway network

[Highway networks paper](https://arxiv.org/pdf/1505.00387.pdf)

[HIGHWAY AND RESIDUAL NETWORKS LEARN
UNROLLED ITERATIVE ESTIMATION](https://arxiv.org/pdf/1612.07771.pdf)


Bonus read:
[Convolutional Networks](https://ujjwalkarn.me/2016/08/11/intuitive-explanation-convnets/)

## License

MIT License

Copyright (c) 2017 Luka Anicin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
