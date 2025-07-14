Retrieval Augmented Generation (RAG) application

# REQUIREMENTS:

NOTE: For any installation you do not know yet, please check YouTube for a video tutorial on how to install it.

You should have installed:

- Python 3.13.2
- Visual Studio Code
- Ollama (for utilizing a language model)
- Llama 3.2 model (or any model efficient for your laptop/PC)
- nomic-embed-text model (for embedding)

# PROCESS:

NOTE: The double asterisks (\*\*) represents the beginning and end of syntax written below.

1. Create a folder to contain the entire project. For example, Let's assume the name this folder is "RAG".

2. Create a virtual environment by running the syntax below in your folder named "RAG":

   ** python -m venv RAG_env **

3. Activate your virtual environment by opening the terminal and navigating to the "Scripts" directory in "RAG_env". For this, go to the terminal and input the syntax below:

   ** .\RAG_env\Scripts\activate **

4. Install the necessary packages listed in the "requirements.txt" file, which can be found in the "RAG" folder. For this, go to the terminal and input the syntax below:

   ** pip install requirements.txt **

5. Create a file named ".env" in your the "RAG" folder.

6. Generate an API key from Langsmith by going to "langsmith.com" on your web browser, creating an account. After that, click the "Set up tracebility" option at the top of your account page, then click "Generate API key" under the "With Langchain" option.

7. Now copy your generated API key along with the extra set of details and paste them in the ".env" file. What you copy should look like this:

   **
   LANGSMITH_TRACING=true
   LANGSMITH_ENDPOINT="https://api.smith.langchain.com"
   LANGSMITH_API_KEY="\*\***\*\*\*\***\*\***\*\***\*\***\*\*\*\***\*\***"
   LANGSMITH_PROJECT="RAG"
   \*\*

8. Create a folder named "Vector_Store" in the main "RAG" folder. This folder will be used to store the vector store files.

9. Start the Ollama server in order to use the LLM and embedding models by going to the terminal of VS code or Command Prompt and inputting the syntax below:

   ** ollama serve **

# SUGGESTIONS FOR IMPROVEMENT:

1. Switch from "Text-structure based" text splitting (RecursiveCharacterTextSplitter) to "Semantic-meaning based" text splitting for improved semantic retrieval. Consider "SemanticChunker" at https://python.langchain.com/docs/how_to/semantic-chunker/

2. Consider an Embedding model with a larger context window for improved context coherence.

3. Consider switching from local development to production ready deployment using API keys e.g. from OllamaEmbeddings nomic model to nomic API key, from FAISS vector store to Qdrant vector store .

4. Implement more sophisticated retrieval techniques such as:
   i. A better vector store like Qdrant or Pinecone.

   ii. A more advanced retriever like BM25retriever or Dense Retriever.

   iii. A combination of multiple retrievers.

   iv. A retriever agent like RAGRetriever or RetrievalQA.

   v. Query analysis to transform or construct optimized search queries from raw user input.
