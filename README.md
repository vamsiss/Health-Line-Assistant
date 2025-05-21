# HealthLine Assistant

A medical knowledge assistant that leverages RAG (Retrieval-Augmented Generation) to provide accurate healthcare information by combining document retrieval with LLM generation.

## Overview

HealthLine Assistant is an AI-powered medical information system that:
- Processes medical textbooks and documents
- Provides accurate medical information through conversational AI
- Uses RAG architecture to ground responses in reliable sources
- Ensures factual accuracy while maintaining natural dialogue

## Technologies Used

### Core Technologies
- Python 3.10
- LangChain
- OpenAI API
- Pinecone Vector Database
- Sentence Transformers
- Flask (Web Framework)

### Key Libraries
- langchain
- langchain-openai 
- langchain-pinecone
- sentence-transformers
- python-dotenv
- PyPDF2
- Flask

## Project Structure

```
HealthLine-Assistant/
├── Data/                   # Medical documents and PDFs
├── src/                    # Source code
│   ├── helper.py          # Helper functions
│   └── store_index.py     # Vector store indexing
├── research/              # Research notebooks
│   └── trials.ipynb       # Development notebook
├── requirements.txt       # Project dependencies
└── .env                  # Environment variables
```

## Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/KethanPilla/HealthLine-Assistant.git
cd HealthLine-Assistant
```

2. Create and activate virtual environment:
```bash
conda create -n healthLineAssistant python=3.10
conda activate healthLineAssistant
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables in `.env`:
```
PINECONE_API_KEY=your_pinecone_api_key
OPENAI_API_KEY=your_openai_api_key
```

5. Place medical documents in the `Data/` directory

6. Run the indexing script:
```bash 
python src/store_index.py
```

## How It Works

1. **Document Processing**
   - Loads medical PDFs from Data/ directory
   - Splits documents into chunks
   - Creates embeddings using Sentence Transformers

2. **Vector Storage**
   - Stores document embeddings in Pinecone
   - Enables semantic search capabilities
   - Maintains context for retrieval

3. **RAG Pipeline** 
   - Retrieves relevant passages based on queries
   - Augments LLM prompts with retrieved context
   - Generates accurate responses grounded in sources

4. **Response Generation**
   - Uses OpenAI API for natural language generation
   - Combines retrieved context with conversational AI
   - Ensures responses are factual and helpful

## Usage

1. Import the required modules
2. Initialize the assistant with your API keys
3. Query medical information through the provided interface
4. Receive accurate, source-grounded responses

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Medical document providers
- Open source AI/ML community
- Project contributors

## Contact

Sai Tumpati - [GitHub](https://github.com/vamsiss)
