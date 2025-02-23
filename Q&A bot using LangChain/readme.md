# RAG Chatbot with LangChain and IBM Watsonx

## Overview
This is a Retrieval-Augmented Generation (RAG) chatbot built using LangChain and IBM Watsonx. The chatbot allows users to upload a PDF document and ask questions, retrieving relevant information from the uploaded document.

## Features
- **PDF Document Loader**: Loads and processes PDF documents.
- **Text Chunking**: Splits documents into smaller chunks for efficient retrieval.
- **Vector Database**: Uses Chroma for storing and retrieving document embeddings.
- **LLM-based QA**: Utilizes IBM Watsonx Large Language Model for answering questions.
- **Gradio Interface**: Provides a simple UI for user interaction.

## Technologies Used
- **IBM Watsonx** (WatsonxLLM, WatsonxEmbeddings)
- **LangChain**
- **Chroma Vector Store**
- **Gradio**

## Installation
Ensure you have Python installed (preferably 3.8 or later). Install dependencies using:
```sh
pip install langchain langchain_ibm gradio chromadb ibm-watsonx-ai pypdf
```

## Usage
1. Run the application:
```sh
python qabot.py
```
2. Open your browser and navigate to `http://localhost:7860`
3. Upload a PDF file.
4. Type a question related to the document.
5. Get responses based on document content.

## File Structure
```
qabot.py            # Main script for the chatbot
README.md           # Project documentation
```

## How It Works
1. **Document Processing**: The chatbot loads the uploaded PDF and splits it into text chunks.
2. **Embedding & Storage**: Chunks are converted into embeddings using IBM Watsonx and stored in ChromaDB.
3. **Retrieval & Answering**: User queries are matched with stored chunks, and the most relevant ones are passed to the IBM Watsonx LLM for response generation.



