

# PDF Reader with LLaMA 2 7B and RAG

## Overview
This project implements a **PDF Reader** using **LLaMA 2 7B** and a **Retrieval-Augmented Generation (RAG)** approach. The system downloads PDF files from **MongoDB**, processes them into a retrievable format, and answers user queries based on the stored content. The project also includes a **testing framework** to evaluate the model's performance using a dataset.

## Features
- **PDF Retrieval**: Downloads PDF files from MongoDB.
- **Text Extraction**: Extracts text from PDFs for processing.
- **Embedding and Indexing**: Converts text into vector embeddings for efficient retrieval.
- **Query Handling**: Uses RAG with **LLaMA 2 7B** to generate accurate responses.
- **Testing Framework**: Evaluates the model's performance against a benchmark dataset.

## Technologies Used
- **LLaMA 2 7B**: Language model for text generation.
- **MongoDB**: Stores and retrieves PDF files.
- **ChromaDB**: Vector database for embedding-based retrieval.
- **LangChain**: Manages LLM-based retrieval and query processing.
- **PyMuPDF**: Extracts text from PDFs.
- **Hugging Face Transformers**: Loads the LLaMA 2 7B model.
- **Pytest**: Framework for testing model accuracy.

## Installation
1. **Clone the Repository**  
   ```sh
   git clone https://github.com/yourusername/pdf-reader-llama.git
   cd pdf-reader-llama
   ```

2. **Install Dependencies**  
   ```sh
   pip install -r requirements.txt
   ```

3. **Set Up MongoDB Connection**  
   Modify the `config.py` file with your MongoDB credentials:
   ```python
   MONGO_URI = "your_mongo_connection_string"
   MONGO_DB = "your_database_name"
   ```

4. **Run the Application**  
   ```sh
   python main.py
   ```

## Usage
1. **Upload PDFs**  
   - Store PDF files in MongoDB manually or through an API.
   
2. **Query the Model**  
   - Run the script and enter your queries:
     ```sh
     python query.py --question "What does the document say about AI?"
     ```
   
3. **Testing the Model**  
   - The `test.py` script evaluates the model using a dataset:
     ```sh
     pytest test.py
     ```
   - The test framework compares LLaMA 2 7B’s responses with expected answers.

## Future Enhancements
- Implement **web-based UI** for easy interaction.
- Integrate **fine-tuning** for domain-specific improvements.
- Optimize **embedding storage** for faster retrieval.

---
Developed by **Humayun Abdullah** 🚀
