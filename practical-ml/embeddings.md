# Embeddings

Embeddings are numerical representations of ML features used as input to deep learning models.
aka. Deep learning models’ internal representations of their input data.

Embeddings aren't the data inputs or ouput results -- they are data that has been transformed into n-dimensional matrices for use in deep learning computations.

## Vectors

Example of a single embedding (aka. a vector) in 3 dimensions:
```
[1 4 9]
```
This is a representation of a single element in the dataset, eg the word "fly".

Generally, individual embeddings are represented as row vectors.

## Tensor (aka. matrix)

A multidimensional combination of vector representations of multiple elements.

```
[1 4 9]
[4 5 6]
```
These embeddings are the outpot of the process of **learning** embeddings, done by passing raw data into an ML model.

This multidimensional input data gets transformed via compression through algorithms into a lower-dimensional space.

The result is a st of vectors in an **embedding space**.

Multimodal data ---> algorithm --> embedding space
(word/sentence/image)             

## Embedding Process

- Transforms multimodel input into vectors, tensors, graphs, etc (vectors can be thought of as an array of numbers here)
- Compresses input info for use in an ML task. This process changes variable feature dimensions into fixed inputs to be passed downstream
- Creates an **embedding space** specific to the data the embeddings were trained on but can be generalized to other domains/tasks (aka. transfer learning - the ability to switch contexts)



### Resources to check out
- https://openai.com/blog/introducing-text-and-code-embeddings
- https://platform.openai.com/docs/guides/embeddings
- https://vickiboykis.com/what_are_embeddings
- https://stack.convex.dev/the-magic-of-embeddings
- https://www.pinecone.io/learn/vector-embeddings/