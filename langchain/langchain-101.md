# LangChain

A Python/JS framework for building AI applications that abstracts interacting with LLMs.

## Core components

- LLMs
- prompt templates
- memory
- agents
- embeddings/vector stores

## Prompt Templates

### Few Shot Prompt Templates

- **parametric knowledge** = knowledge learned by the model during training time and is stored within the model weights/parameters
- **source knowledge** = knowledge provided ot the model at inference time, via input prompt

LangChain has a `FewShotPromptTemplate` that's good for source knowledge input. 

### Resources
- [Pinecone's LangChain AI Handbook](https://www.pinecone.io/learn/series/langchain)
- https://learnlangchain.streamlit.app/