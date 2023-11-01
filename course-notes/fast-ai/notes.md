# fast.ai's Practical Deep Learning for Coders course (2022)

https://course.fast.ai

## Lesson 1

- With neural networks, you don't need to build features, they do it for you.
- We don't give neural networks features, we ask it to learn features (don't have to come up with these ideas).
- The higher layers get more advanced in terms of what features they find
- You start with a random NN and feed it examples

- You can use image recognizers on other things (eg. sound, computer mouse systems, etc)

### fastai lib
- abstracts Pytorch
- **learner** - something that combines a model (the NN func), the data we're training with
  - [timm](https://timm.fast.ai) - the largest collection of computer vision models in the world
  - fast.ai is one of the few frameworks that integrate it
- Someone else has already trained the model to recognize ImageNet dataset. They made the weights available.
- by default fast.ai downloads the weights for you
- fast.ai's `fine_tune` method: teaches the model the differences between your dataset and what it was originally trained for

Step 3: Use model (and build own)

## Tabular analysis

- uses `fit_one_cycle` (instead of `fine_tune`), since there's not likely a pre-trained model that works for your tabular dara since tabular data tends to be very case specific

## Collaborative Filtering

- "which users liked which products" -> find similar users


### Misc

What people use in research is a strong leading indicator of where industry is going


## Lesson 2

- **data augmentation** getting different pictures each time from the same image

- tip: before data cleaning, buidl a model to find out what things are difficult to recognize in your data and find the things the model can help you find data problems