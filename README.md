# AI-Powered Document QA with Google Drive, OpenAI, and Pinecone (n8n Workflow)

This n8n workflow automates the ingestion of a PDF from Google Drive, converts it into vector embeddings using OpenAI, stores them in Pinecone, and enables document-based question-answering via a chatbot interface.

---

## Features

- Downloads files from Google Drive
- Extracts and splits text content into chunks
- Generates embeddings using OpenAI
- Stores embeddings in a Pinecone index
- Enables real-time chatbot Q&A on uploaded content

---

## Workflow Breakdown

### 1. Manual Trigger
Starts the workflow manually for testing or development.

### 2. Set Google Drive File URL
Uses a static `Set` node to assign the file URL.

### 3. Download File
Downloads the file from Google Drive using the OAuth2 credentials.

### 4. Data Processing
- Loads the binary file
- Splits content using Recursive Character Text Splitter
- Converts chunks into embeddings via OpenAI

### 5. Store in Pinecone
- Embeddings are inserted into the `n8nfilesdemo` index
- Previous data is cleared to prevent duplication

### 6. Chat Trigger
Listens for incoming chat messages (from a UI or API).

### 7. OpenAI Chat Model
Handles natural language interactions using the GPT-4o-mini model.

### 8. Retrieval Agent
Queries Pinecone using user messages and responds with relevant information.

---

## Requirements

- n8n (self-hosted or cloud)
- Pinecone account and API key
- OpenAI API key
- Google Drive API credentials

---

## Setup Instructions

1. Clone this repository and open the workflow in n8n.
2. Set your credentials for Google Drive, OpenAI, and Pinecone.
3. Update the file URL in the `Set` node.
4. Run the workflow manually or integrate the chat trigger.


