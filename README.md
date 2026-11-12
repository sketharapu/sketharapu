## Hi, I'm Sreekanth Reddy Ketharapu 👋

I work on machine learning, mostly on making large language models and vision-language models
run fast on a single local GPU, and measuring what actually helps.

### What I'm working on

- **Speculative decoding at long context.** In vLLM, MTP and DFlash drafters fall behind plain decoding
  past about 21K prompt tokens (0.54x at 64K). The cause is the verify step's attention not splitting the
  KV cache; routing it through a split-KV kernel brings DFlash to 1.39x plain decoding at 64K.
- **Local inference benchmarks.** vLLM, SGLang and llama.cpp on the same models and prompts.
- **Document extraction with VLMs.** Fine-tuning Qwen3-VL to fill a JSON schema with word-level
  bounding boxes (SFT, then GRPO).

### Open source

- [Strata](https://github.com/Niko1221/Strata): bug report on `strata launch --vision gpu` starting
  without its DFlash2 drafter ([#5810](https://github.com/Niko1221/Strata/issues/5810))

### Earlier projects

- [RAG_agents](https://github.com/sketharapu/RAG_agents): CrewAI agents that route a question to a
  PDF vector store or to web search (Llama 3 on Groq, BGE embeddings, Tavily).

**Tools:** Python · PyTorch · vLLM · SGLang · llama.cpp · Hugging Face Transformers · ms-swift · Triton · CrewAI / LangChain

**Background:** M.S. in Artificial Intelligence – University of Michigan
