## Setup Instructions

### Installation

Make sure to install the required packages before running the notebook:
```bash
!pip install langchain_openai python-dotenv streamlit langchain_community langserve fastapi uvicorn sse_starlette bs4 chromadb faiss-cpu gradio pypdf
```

### Environment Variables

Ensure to set the following environment variables:
- `OPENAPIKEY`: Your OpenAI API key

## Usage

### Running the Script

1. Upload your files:
   - Choose between PDF files, text files, or provide a web link.

2. Select the appropriate mode:
   - **PDF File**: Upload a PDF file to query.
   - **Text File**: Upload a text file to query.
   - **Web Link**: Provide a web link to extract and query content.

3. Submit your query:
   - Enter your query to search within the uploaded document or web link.

4. Interact with Doc Bot:
   - The bot will provide responses based on your queries.

### Functions

- **web_link(link=None, query=None)**: Function to process web links and queries.
- **pdf_file(path, message)**: Function to process PDF files and queries.
- **text_file(path, message)**: Function to process text files and queries.
- **echo(message, history)**: Echo function for handling user inputs and chat history.

### Global Variables

- **user_mode**: Current mode selected (PDF File, Text File, Web Link).
- **path_file**: Path to the uploaded file for current mode.

## Note

- This notebook uses OpenAI's GPT-3.5 for text responses.
- Make sure to handle large files appropriately due to processing constraints.

---

