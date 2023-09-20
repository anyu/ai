# Choosing between different generative AI approaches

## Comparing common approaches

From lowest effort / least accurate / most flexibile to highest effort / most accurate / least flexible:

1. **Prompt Engineering**: providing context with few examples (aka. few-shot learning) to make an FM learn your use case.
  -  least accurate
2. **RAG (Retrieval Augmented Generation)** : augmenting use-case specific context from vectorized DBs
  - aka "grounded generation" (?)
  - higher accuracy results than prompt engineering, with lower changes of hallucinations
  - need to create embeddings and set up vector stores
  - may need to pay for: embedding model, vector store, FM
  - high flexibility: can change each component independently
3. **Fine-tuning**: updating model weights on domain specific data
  - higher accuracy results than RAG
  - model's weight/parameters get changed via tuning scripts
  - can be done with very little data (?)
  - getting the tunable param values right takes time
  - lower flexibility: need to retune every time there's a base model version update or new data. More effort to adapt fine-tuned model to different use cases.
4. **Training your own FM (foundational model) from scratch**: training model on use-case specific data from scratch
  - highest accuracy results, close to no hallucinations
  - requires gathering/curating data, designing the model architecture, experimenting with different modelling approaches to find optimal model
  - highest costs with end-to-end data processing, ML training, tuning, deployment
  - least flexible: updates may require a re-training cycle. In some cases the model can be fine-tuned, but accuracy varies.

  ## Use case guidance

  - Use **prompt engineering** when use case doesn't contain much domain context
  - Use **RAG** when you want a lot of flexibility with different components
  - Use **fine-tuning** when you want more control over the model + data is very domain specific
  - **Train from scratch** when none of the above works + you have vast data points + hardware infra

  ### Resources
  - [Why You (Probably) Don't Need to Fine-tune an LLM](https://www.tidepool.so/2023/08/17/why-you-probably-dont-need-to-fine-tune-an-llm)