# DocQuery

A robust document retrieval and question-answering system powered by RAG (Retrieval Augmented Generation) technology. This project combines the power of Pinecone vector database, OpenAI GPT, and advanced embedding techniques to create an intelligent document querying system.

## 🌟 Features

- **PDF Processing**: Automatically converts PDF documents into searchable chunks while maintaining context
- **Vector Search**: Utilizes Pinecone's vector database for efficient similarity search
- **Intelligent Responses**: Leverages OpenAI GPT/CoPilot for generating natural language responses
- **Multilingual Support**: Uses multilingual-e5-large model for embeddings
- **Scalable Architecture**: Built with serverless infrastructure on AWS

## 🛠️ Technologies Used

- Python 3.10+
- Pinecone Vector Database
- OpenAI GPT-3.5
- CoPilot API (alternative)
- PyPDF2 for PDF processing
- AWS (for serverless Pinecone deployment)

## 📋 Prerequisites

- Python 3.10 or higher
- Pinecone API key
- OpenAI API key (or CoPilot API key)
- Required Python packages (see requirements section)

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/yourusername/docquery.git
cd docquery
```

2. Install required packages:
```bash
pip install pinecone-client openai pypdf2 requests
```

3. Set up your environment variables:
```python
OPENAI_API_KEY = "your-openai-api-key"
PINECONE_API_KEY = "your-pinecone-api-key"
```

4. Initialize the Pinecone index:
```python
pc, index = initialize_pinecone()
```

5. Start querying your documents:
```python
question = "Your question here"
answer = answer_question(pc, index, question)
print(answer)
```

## 💡 Usage Example

```python
# Convert PDF to searchable documents
pdf_path = "your_document.pdf"
docs = convert_pdf_to_docs(pdf_path)

# Initialize Pinecone
pc, index = initialize_pinecone()

# Ask questions
question = "What are the system requirements?"
answer = answer_question(pc, index, question)
print(answer)
```

## 🔧 Configuration

The project supports two different LLM backends:
1. OpenAI GPT-3.5
2. CoPilot API (as a free alternative)

You can switch between them by using either `answer_question()` or `answer_question_copilot()` functions.

## 📝 Notes

- The system requires an active internet connection for API calls
- PDF processing is done in chunks for better context preservation
- Vector embeddings are generated using the multilingual-e5-large model
- The Pinecone index is configured for serverless deployment on AWS

## ⚠️ Limitations

- OpenAI API requires a paid account with sufficient credits
- Large PDF files might take longer to process
- Internet connection is required for all operations

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

