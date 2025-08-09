
Admission Chatbot (PDF QA System)
==============================================

Overview
--------
This project is an AI-powered Admission Chatbot that can answer queries directly from the 
NIT Rourkela JoSAA/CSAB Admission Guidelines PDF or any other structured admission-related document.

It uses LangChain, FAISS, and OpenAI GPT to:
- Read and understand official admission documents.
- Retrieve relevant information quickly.
- Answer student queries accurately with references from the document.

Features
--------
- PDF Parsing & Processing – Loads and splits official admission PDFs into searchable chunks.
- Semantic Search – Uses OpenAI Embeddings & FAISS for high-accuracy information retrieval.
- Structured Query Understanding – Extracts key query details like section, clause type, and keywords.
- Hybrid Retrieval – Combines semantic search with rule-based filtering for precise matches.
- Parallel Reasoning – Evaluates document sections in parallel for faster processing.
- Optimized Answer Generation – GPT provides clear, factual, and context-backed responses.
- Query Caching – Stores query analysis results for repeated questions, speeding up responses.

Tech Stack
----------
- Python 3.10+
- LangChain – LLM orchestration & retrieval pipelines
- LangGraph – State-based query execution
- FAISS – Vector similarity search
- OpenAI GPT – Language model for reasoning & answering
- PyPDFLoader – PDF parsing
- Sentence Transformers – Embedding generation
- Rich – Beautiful CLI output

Quick Start
-----------
1. Clone this repository
   git clone https://github.com/yourusername/admission-chatbot.git
   cd admission-chatbot

2. Install dependencies
   pip install -r requirements.txt

3. Set API Keys
   export OPENAI_API_KEY="your_openai_api_key"
   export LANGCHAIN_API_KEY="your_langchain_api_key"

4. Run the Chatbot
   from main import create_optimized_rag_system, ask_question_optimized

   system = create_optimized_rag_system("data/admission.pdf")
   ask_question_optimized(system, "When will classes start for the 2023-24 UG programmes?")

Example Queries
---------------
- When will the classes start for B.Tech students?
- What is the balance admission fee for OBC students with income between 1-5 lakhs?
- Where should boys report during admission?
- What documents are needed for admission?

Use Cases
---------
- Answer prospective student queries instantly.
- Assist college help desks during admission season.
- Reduce manual search time in lengthy PDFs.
