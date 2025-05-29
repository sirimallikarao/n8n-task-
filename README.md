RAG Knowledge Base with Google Drive Integration
An intelligent document Q&A system built with n8n that automatically processes documents from Google Drive and enables conversational queries using OpenAI and Pinecone vector search.
Features

Document Ingestion: Automatically downloads and processes documents from Google Drive
Vector Storage: Uses Pinecone for efficient semantic search and retrieval
Smart Text Processing: Implements recursive character text splitting with configurable chunk sizes (3000 chars, 200 overlap)
AI-Powered Chat: OpenAI GPT-4o-mini integration for natural language responses
RAG Architecture: Retrieval-Augmented Generation for accurate, context-aware answers
Real-time Chat: Webhook-based chat interface for instant responses

Workflow Components

Document Processing Pipeline:

Manual trigger for workflow testing
Google Drive file download
Document loading and text splitting
Vector embedding generation (OpenAI)
Storage in Pinecone vector database


Query Processing:

Chat trigger for user interactions
Vector similarity search in knowledge base
AI agent with access to specialized knowledge tool
Contextual response generation



Use Cases

Technical documentation Q&A systems
Knowledge base chatbots
Document analysis and insights
Customer support automation
Internal company knowledge sharing

Prerequisites

n8n instance
Google Drive API credentials
OpenAI API key
Pinecone account and API key

Perfect for organizations looking to build intelligent document search and Q&A systems with minimal setup complexity.
