# Context Engineering Demo with LangChain and OpenAI

This project demonstrates a simple example of **context engineering** to improve AI responses using LangChain, OpenAI, and FAISS vector search. The demo compares answers from a language model without context vs. with relevant retrieved context from a small knowledge base.

---

## Features

- Converts text data into vector embeddings using OpenAIEmbeddings  
- Stores and searches embeddings efficiently with FAISS  
- Uses a conversational retrieval chain to combine retrieval with LLM responses  
- Shows side-by-side comparison of answers without and with context  
- Interactive web interface built with Gradio for easy testing  

---
Demo 🎯

<img width="1409" alt="context_engineering_demo.png" src="context_engineering_demo.png">

## Installation

Make sure you have Python 3.8+ installed.

Install the required packages:
```bash
pip install langchain-community langchain-openai faiss-cpu gradio

import gradio as gr
from langchain_openai import ChatOpenAI, OpenAIEmbeddings
from langchain_community.vectorstores import FAISS
from langchain.text_splitter import CharacterTextSplitter
from langchain.chains import ConversationalRetrievalChain
from langchain.memory import ConversationBufferMemory

