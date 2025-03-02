# MediChat-LLM

An end-to-end medical chatbot built using LLaMA2, designed to provide healthcare information and assistance.

## Overview

MediChat-LLM uses a fine-tuned LLaMA2 model to provide contextual medical information. The system employs vector embeddings through Pinecone for efficient context retrieval and uses a Flask web interface for user interactions.

## Features

- Medical knowledge base integration via vector embeddings
- Contextual conversation handling
- Web-based user interface
- Prompt engineering optimized for medical conversations

## Installation

### 1. Clone the repository:
```bash
git clone https://github.com/mahmouddbelo/MediChat-LLM.git
cd MediChat-LLM
```

### 2. Create a virtual environment:
```bash
conda create -n medchat python=3.10 -y
```

### 3. Activate the environment:
```bash
conda activate medchat
```

### 4. Install the requirements:
```bash
pip install -r requirements.txt
```

### 5. Set up environment variables:
Create a `.env` file in the root directory with your Pinecone credentials:
```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### 6. Download the LLaMA2 model:
Download the quantized model and place it in the model directory:
```
llama-2-7b-chat.ggmlv3.q4_0.bin
```
The model can be downloaded from:
https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main

### 7. Initialize the vector store:
```bash
python store_index.py
```

### 8. Run the application:
```bash
python main.py
```

### 9. Access the application:
Open your browser and navigate to `http://localhost:5000`

## Project Structure

- `main.py`: Main Flask application
- `setup.py`: Setup script for initial configuration
- `template.py`: Template definitions for prompts
- `src/`: Source code directory
  - `helper.py`: Helper functions
  - `prompt.py`: Prompt engineering functions
- `templates/`: HTML templates
  - `chat.html`: Chat interface
- `model/`: Directory for storing the LLaMA2 model files
- `data/`: Data storage directory containing medical knowledge base

## Tech Stack

- **Python**: Core programming language
- **LangChain**: Framework for working with language models
- **Flask**: Web application framework
- **Meta LLaMA2**: Large language model for generating responses
- **Pinecone**: Vector database for efficient knowledge retrieval

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- LLaMA2 by Meta AI
- Pinecone for vector database services
- LangChain for the LLM framework
