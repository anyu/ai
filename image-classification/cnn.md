# CNN (Convolutional Neural Networks)

A type of "feed-forward" neural network that learns feature engineering by itself via filters (aka kernel) optimization.

Used to extract higher and higher level representations of an image.

Instead of pre-processing data to derive features, a CCN takes the image's raw pixels as input and "learns" how to extract features.

1. A **convolution** extracts tiles of the input feature map -> applies filters to them to compute new fatures -> produces an output feature map (aka. convolved feature)

During convolution, the filters slide over the input feature's map grid horizontally + vertically, a pixel at a time.

#### How it works

Takes numerical pixel values of image --> passes through convolution / ReLUs / pooling / fully connected --> output layer.

### CNN's hidden layers

- **Convolutional layer**: Extracts features of an image by scanning through the image w/ filters. Takes an input -> applies a filter -> outputs a feature map.
- **ReLU layer** (rectified linear units): takes the output of the convolution layer + rectifies negative values to zero. Adds non-linearity to the model.
- **Pooling layer** - a filter runs over the input matrix and assigns a value per subregion to a new output matrix. The goal is to downsize an image.
- **Fully connected layer (the final layer)**: Takes the output of the last pooling layer as input, and aggregates all info to generate final classification.

One value may suggest the paw in the image belongs to a dog. Another value may suggest the nose. The fully connected layer combines all this information, applies weights, to produce the output.

### Resources
- https://levity.ai/blog/how-do-image-classifiers-work#:~:text=Image%20classifiers%20rely%20on%20Convolutional,layer%2C%20and%20fully%20connected%20layer.