# Chat with PDF using Gemini

## Overview
This project is a Streamlit-based web application that allows users to upload PDF files, process their content, and ask questions about the extracted text. It leverages Google Generative AI (Gemini) for embeddings and question answering, FAISS for vector storage, and LangChain for conversational chains. Users can interact with the app through a simple interface to query information from uploaded PDFs.

## Code Description
The codebase consists of:
- **PDF Processing**: Extracts text from uploaded PDFs using PyPDF2.
- **Text Chunking**: Splits the extracted text into manageable chunks using RecursiveCharacterTextSplitter.
- **Vector Store**: Creates embeddings with GoogleGenerativeAIEmbeddings and stores them in a FAISS index for similarity search.
- **Question Answering**: Uses a conversational chain powered by ChatGoogleGenerativeAI (Gemini-pro model) to answer user questions based on the PDF content.
- **UI**: A Streamlit interface for uploading PDFs, processing them, and querying the content.

Key files:
- `app.py`: The main script containing all functionality (PDF processing, vector storage, and question answering).
- `.env`: Stores the Google API key (not included in the repo; must be set up manually).

## How to Run the Code
1. **Create Virtual Environment**:
    Step 1:Create a new directory for your project and Navigate to the project directory.
    Step 2: Create a virtual environment using venv.
        python -m venv .venv
    Step 3: Activate the virtual environment. 
        .venv\Scripts\activate
   
    (Here .venv is virtual_environment_name)

2. **Pre-requisites**:
   - Python 3.8+
   - Install dependencies: 
     ```bash
        pip install requirements.txt

3. **Run**:
    streamlit run app.py

