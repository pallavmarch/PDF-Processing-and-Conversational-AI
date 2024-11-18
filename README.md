# PDF Processing and Conversational AI with Falcon-7B

This project combines the power of natural language processing (NLP) and conversational AI to enable users to process PDF documents and interact with their content through a user-friendly interface. The solution is built using **Hugging Face's Falcon-7B** model for generating contextual responses, **FAISS** for vector-based similarity search, and **Gradio** for an interactive UI.

---

## Features

- **PDF Processing**: Extracts text from uploaded PDF files and organizes it into chunks for efficient search and retrieval.
- **Contextual Search**: Embeds text using `sentence-transformers` and stores them in a FAISS vector store for high-performance similarity search.
- **Conversational AI**: Answers user queries based on PDF content using the Falcon-7B language model from Hugging Face.
- **Interactive UI**: Built with Gradio for an easy-to-use web interface.

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pdf-falcon-chat.git
   cd pdf-falcon-chat
   ```

2. Install the required dependencies:
   ```bash
   pip install gradio PyPDF2 langchain-community sentence-transformers transformers
   ```

3. Download the Falcon-7B model (or replace with another compatible model if needed).

---


## Code Overview

### Core Components

- **Text Embedding**: 
  Utilizes `sentence-transformers` to convert text chunks into embeddings for efficient similarity search.

- **Vector Store**: 
  Stores embeddings in a FAISS index for high-performance nearest-neighbor search.

- **Conversational AI**: 
  Leverages Falcon-7B to generate contextual answers based on extracted text.

- **Gradio Interface**: 
  Provides an intuitive UI for users to upload PDFs and interact with the application.

### Key Libraries

- `transformers`: For loading and interacting with Falcon-7B.
- `sentence-transformers`: For creating text embeddings.
- `PyPDF2`: For extracting text from PDF files.
- `langchain`: For vector-based document search with FAISS.
- `gradio`: For building the user interface.

---

## Example Workflow

1. **Upload PDF Files**:
   - Select the "Process PDFs" task.
   - Upload your PDF files and process them.

2. **Ask Questions**:
   - Switch to the "Ask Question" task.
   - Type a question and get a response based on the uploaded PDFs' content.
