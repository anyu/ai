## LLMs

Notes from [Simon Willison's blog](https://simonwillison.net/2023/Aug/3/weird-world-of-llms/#what-they-are).

### How they work

LLMs are essentially libraries. Or you can think of them as functions.

They guess next words. Technically, next tokens.

Each word has a token (integers between 1 to 30k).

- `The` = `464`
- `the` = `262`

## Training data

Most companies aren't sharing data their LLMs are trained on, but LLaMA's is [public](https://arxiv.org/abs/2302.13971). 5 TB of data:
- 67% from CommonCrawl
- 15% from C4
- rest from Github, Wikipedia, 'books' (Project Gutenberg, Books3), ArXiv (scholarly articles), StackExchange

Other part of data = RLHF - reinforcement learning from human feedback.

## How LLM tokenizers work

TODO: 
- https://simonwillison.net/2023/Jun/8/gpt-tokenizers/
- OpenAPI tokenizer tool: https://platform.openai.com/tokenizer

## Timeline

- 2015: OpenAPI founded.
- 2018: OpenAPI releases GPT-1, a basic language model
- 2019: OpenAI releases GPT-2
- 2020: OpenAPI releases GPT-3. Earlier adopters take notice.
- 2022 November: OpenAPI releases ChatGPT.
- 2023: LLaMA, Alpaca, Bard, PaLM, GPT-4, PaLM 2, Claude, Falcon, Llama 2

## Key LLM Models (as of Sep 2023)

- **ChatGPT (GPT-4)**. Cheapest and fastest. Free via MS Bing. 8k token limit. Data from up to Sep 2021.
- **Claude 2**. Anthropic's (an OpenAPI spin off). Free. Same as CGPT but with higher limit - 100k tokens.
- **Bard**. Google's, based on PaLM 2.
- **Llama 2**. Meta's. The leading openly licensed model. The first good model that technically is allowed for commercial uses.

## Good use cases

- code (API design supposedly)
- explaining / summarizing jargon
- generating names for things
- get 20 ideas for X. First 10 is usually obvious.

## Tools to try out

- Embeddings API: https://platform.openai.com/docs/guides/embeddings/what-are-embeddings
- ChatGPT plugins: https://openai.com/blog/chatgpt-plugins
- ChatGPT Code Interpreter: write Python code and run in a repl type env