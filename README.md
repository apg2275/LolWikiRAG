# LolWikiRAG
An Language Model (LLM) Retriever-Augmented Generation (RAG) using data scraped from the [League of Legends Wiki](https://leagueoflegends.fandom.com/) with a focus on trying to answer questions regarding gameplay interactions for League of Legends while being able to answer basic questions as well.

Built mainly using [Llama Index](https://github.com/run-llama/llama_index).

Finetuned vector embeddings were based off of [BAAI's BGE EN Base v1.5](https://huggingface.co/BAAI/bge-base-en-v1.5) then finetuned for improved performance as seen here

# Methodology
 - Generate a list of pages to scrape. As well scrape all LolWiki pages that are linked on each page
 - Use BeautifulSoup to extra the text for embed testing and keep a separate HTML version for RAG's HTML parser
 - Create a separate vector store for each category
 - Treat each vector store as it's own retriever and add metadata descriptions
 - Create a Router Retriever that uses the descriptions to retrieve documents from multiple vector indexes.
 - Create Query Pipeline
 
# Examples
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/a112253c-2115-4519-939a-e274b282c0bf)
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/eef19b29-c43c-4ec6-8e90-4767f1cd57b5)

![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/e93453a8-6635-498d-b1d3-703c2547ef6a)
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/799f2461-ca8b-4637-b96e-39cc13aa1641)

![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/e2e07a60-7c27-406e-8d04-cd4d22a57785)
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/33cb3b91-6fb1-4be4-ac1b-1f2be1c5ec69)

![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/f4f593a4-bc65-4eea-ba9d-89c9fd9c9b13)
![image](https://github.com/apg2275/LolWikiRAG/assets/89856165/b35dc3de-8e5c-4311-84e0-4668ac2e0b29)



# To Do List
- [ ] Add Async
- [ ] Possibly add lore/story information
- [ ] Potential rewrite of LlamaIndex's [UnstructuredElementNodeParser](https://docs.llamaindex.ai/en/v0.9.13/api/llama_index.node_parser.UnstructuredElementNodeParser.html) to include Metadata for more accurate table summaries for better retrieval
- [ ] General optimizations
