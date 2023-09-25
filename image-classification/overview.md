# Image Classification

**Image classification** is a computer visiion task where the goal is to assign a single label/(predefined) category to an entire image.

Common use cases: content-based image retrieval, scene retrieval

Whereas **object detection** identifies objects within an image, but also information about the locations of those objects.

The output includes labels and bounding box coordinates for each detected object.

Common use cases: autonomous driving, surveillance, image-based search

## Image classification methods

### Unsupervised classification

These methods are automated and don't leverage training data. Discovers hidden patterns w/o human intervention.

#### Pattern recognition

- **K-means** (aka. clusterization) is an unsupervised classification algorithm that groups objects into k groups based on their characteristics.
One of the simplest and more popular unsupervised ML algos.
  - Assumes that the number of clusters is known in advance

#### Image clustering

- **ISODATA** (iterative self-organizing data analysis technique) is another unsupervised method used for image classification.
  - Uses Euclidean distance as the similarity measure to cluster data elements into different classes
  - Allows for different number of clusters

### Supervised classification

These methods use previously classified reference samples to train the classifier and subsequently classify unknown data.

#### Maximum likelihood

Used to estimate parameters of a statistical model. Seeks to find parameter values that maximize the liklihood function (which measures how well the model explains observed data)

#### Minimum distance

Used to find the closest match between 2 entities. Measures the disimilarity between 2 data points or distributions.