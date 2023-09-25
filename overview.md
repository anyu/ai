# AI Overview

Getting my bearings on the landscape.

## Terms

Distinguishing easily conflatable terms.

**TLDR**

> **AI** is the broader field of creating intelligent machines. **ML** is a subset of AI that focuses on learning from data, and **DL** is a subset of ML that uses neural networks for complex pattern recognition. 

- **AI**: Machines that mimic human intelligence and cognitive  capabilities. The broadest term.
  - Three main AI categories:
    - Artificial narrow intelligence (ANI) - weak/narrow AI
    - Artificial general intelligence (AGI) - strong/general AI
    - Artificial super intelligence (ASI) - strong/general AI

- **Machine learning**: A subset of AI, focusing on algorithms and models that allow machine to learn from data without being explicitly programmed.
  - supervised learning - requires a labeled dataset for training
  - unsupervised learning - identifies hidden patterns from an unlabeled dataset
  - reinforcement learning - reacts to an environment on their own
- **Deep learning**: A subfield/technique of ML, inspired by the structure and function of the human brain's neural networks.
  - DL is a more advanced and specialized form of ML that requires substantial computational resources.
  - DL algorithms aka. artificial neural networks: Muliple layers of interconnected nodes that process and transform data.
- **Generative AI**: Powered by large ML models that are pre-trained on raw data (often referred to as 'foundational models (FM')) and learn to generate statisfically probably outputs. A subset of FMs are LLMs.
- **LLMs**: Large Language Models.
  - Models trained on trillions of words across many natural language tasks.
  - A language model itself produces a probability distribution over some vocabulary
  - Not all generative AI tools are built on LLMs, but all LLMs are a form of generative AI.

## Areas to understand

### Foundational machine learning

An **algorithm** is the set of instructions and techniques used to train an ML system, while a model is the outcome of applying an algorithm to data, representing the system's learned knowledge. 

Algorithms are like the recipes, and models are the dishes created using those recipes.

#### Examples of algorithms
- **gradient descent**: an optimization algorithm used to minimize a loss function. Works by iteratively adjusting model parameters to find the min value of the loss function.
- **decision trees**: a type of supervised learning algorithm used for both classification and regression tasks. Make decisions by recursively splitting the data into subsets based on the values of input features, eventually reaching a decision at the tree's leaves.
- **clustering**: an unsupervised learning technique used to group similar data based on characteristics. eg. common algorithms = `K-means`, hierarchical clustering
- **anomaly detection**: technique used to identify unusual patterns

#### Examples of models
- **linear regression**: a type of supervised learning algorithm used for predicting a continuous output (numeric value), based on 1+ input features. Assumes a linear relationship between input features and output. Tries to fit a straight line to data.
- **logistic regression**: a type of supervised learning algorithm, used for binary classification tasks. Models probability of an input belonging to one of the classes using the logistic function.
- **neural networks**: a class of ML learning models consisting of interconnected nodes organized in layers (input layer, hidden layers, output layer)

#### More terms
- **corpus**: commonly used term for input dataset (often structured)

### Process

1. Data Collection: Gather relevant data.
2. Data Preprocessing: Clean and prepare data.
3. Feature Selection/Engineering: Choose or create informative features.
4. Model Selection: Pick an appropriate ML algorithm.
5. Training: Adjust model parameters to minimize errors.
6. Validation: Check model performance on validation data.
7. Testing: Assess model performance on unseen data.
8. Deployment: Use the model to make real-time predictions or decisions.

- **bias**: Error introduced by overly simplistic assumptions in an ML model. Underfitting and overfitting.
- **variance**: Error introduced by a model that is too complex and sensitive to small fluctuations in the training data. 
- **cost functions (aka loss functions)**: measure the error between a model's predictions and the actual target values in the training data. The goal of training is to minimize this cost function.
- **regularization**: a technique used to prevent overfitting in machine learning models. It adds a penalty term to the cost function, discouraging the model from learning overly complex patterns in the training data
  - eg. L1 regularization (lasso), L2 regularization (ridge)
- **optimization algorithms**:  used to adjust a model's parameters iteratively during training to minimize the cost function.

### Deep learning
- basics of neural networks
- practical skills for making them work (eg. hyperparameter tuning)
- convolutional neural networks (CNNs)
- recurrent neural networks (RNNs)
- sequence models, attention models 
- transformers: Introduced by 2017 Attention is All You Need paper, replaced RNN and CNNs
- backpropagation: a variant of gradient descent. The most common training algorithm for neural networks. It makes gradient descent feasible for multi-layer neural networks.
- hyperparameter tuning
- gated recurrent unit (GRU)
- long short term memory (LSTM)
- **embeddings**: A low-dimensional space into which you can translate high-dimensional vectors. Embeddings make it easier to do aML on large inputs like sparse vectors representing words. Ideally, an embedding captures some of the semantics of the input by placing semantically similar inputs close together in the embedding space.
- collaborative filtering?
- hidden layers

### Relevant math concepts
- linear algebra (vectors, matrices, manipulating them)
- probability / statistics
- exploratory data analysis

### Software development
- **PyTorch**
  - ML lib based on Torch framework. Originally from FB, now OSS. 
  - Used for DL models
  - Main features: tensor computation w/ GPU support, deep dynamic neural networks
  - high perf replacement for NumPy
  - easily integrated w/ other Python libs (NumPy, SciPy, pandas)

- **JAX**
  - GPU accelerated version of Numpy w/ powerful function transformations
  - very fast
  - steeper learning curve
  - primarily for research tasks
  - lower-level, but can use more abstracted libs such as Flax, Haiku, Equinox, PIX
  - originally from Google Deepmind

- vector DB


