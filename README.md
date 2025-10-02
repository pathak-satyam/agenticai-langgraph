# Chatbot with Router Agents (LangGraph + LangChain)(Agentic AI)
## Overview
This project implements a conversational chatbot that can decide whether a user’s message requires emotional support or a logical, fact-based response.

It uses the LangGraph framework to organize the flow of conversation into nodes and edges, creating a graph-like structure that routes messages appropriately.

The chatbot has two modes of operation:
- Logical mode: provides facts, clear reasoning, and practical solutions.  
- Emotional mode: responds with empathy, compassion, and supportive guidance.  

---

## Architecture
The conversation graph is designed as follows:

- START → Entry point of the chatbot  
- Classifier → Uses an LLM to classify the message as emotional or logical  
- Router → Directs the flow based on the classification  
- Therapist Agent → Handles emotional responses with empathy  
- Logical Agent → Handles logical/fact-based responses  
- END → Conversation output  

Flow:  
START → Classifier → Router → (Therapist | Logical) → END
## Features
- Uses LangGraph for modular agent routing  
- Powered by LangChain LLMs for classification and responses  
- Supports two distinct agent personas (therapist and logical assistant)  
- Interactive CLI chat loop  
## Requirements
- Python 3.10+  
- Install dependencies:
- add .env file with this structure:
GOOGLE_API_KEY=your_api_key_here
  