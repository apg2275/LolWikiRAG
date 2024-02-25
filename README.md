# LolWikiRAG
An Language Model (LLM) Retriever-Augmented Generation (RAG) using data scraped from the [League of Legends Wiki](https://leagueoflegends.fandom.com/) with a focus on trying to answer questions regarding gameplay interactions for League of Legends while being able to answer basic questions as well.

Built mainly using [Llama Index](https://github.com/run-llama/llama_index).

Finetuned vector embeddings were based off of [BAAI's BGE EN Base v1.5](https://huggingface.co/BAAI/bge-base-en-v1.5) then finetuned for improved performance as seen here

# Examples
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/6fd9f613-cd1b-4f22-999a-46b7ed6c9ca0)
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/d28541a2-3964-416a-a7a8-36604659d67f)

# To Do List
- [ ] Add Async
- [ ] Possibly add lore/story information
- [ ] Potential rewrite of LlamaIndex's [UnstructuredElementNodeParser](https://docs.llamaindex.ai/en/v0.9.13/api/llama_index.node_parser.UnstructuredElementNodeParser.html) to include Metadata for more accurate table summaries for better retrieval
- [ ] General optimizations
