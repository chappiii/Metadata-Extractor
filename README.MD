# From PDF to Knowledge Node: A Dual-Prompting LLM Framework for Bibliographic Metadata Extraction

This framework employs **locally hosted Ollama large language models (LLMs)** to extract, refine, and structure bibliographic metadata from academic PDF.

## Features
- Extracts title, authors, DOI, publication year, keywords, countries, and purpose of research.
- Processes PDFs in batches and outputs structured JSON files.

## How It Works
1. Reads PDF Files.
2. Sends the text to LLM for **metadata extraction**.
3. Sends the extracted metadata to LLM again for **correction**.
4. Parses and validates the LLM response.
5. Saves the final structured metadata as JSON.

## Usage Instructions

### 1. Prepare Input Files
- Place PDF documents in the `./pdfs` directory.
- Ensure an Ollama server is running locally with the required model installed.

### 2. Run the Notebook
- Open the project notebook or script.
- **Execute each cell sequentially from top to bottom.**
- The final cell serves as the **entry point of the framework** and initiates batch processing.

## Requirements

- Python ≥ 3.9  
- Local Ollama installation with supported LLM models  
- Python dependencies listed in `requirements.txt`

## Output Example
```json
{
  "papers": [
    {
      "paper_id": "paper123",
      "doi": "10.1234/example.do1",
      "title": "An Example Title",
      "published_year": "2025",
      "author_list": ["Alice Smith", "Bob Jones"],
      "countries": ["USA"],
      "purpose_of_work": "Investigate example techniques",
      "keywords": ["example", "proof of concept"]
    }
  ]
}
```

## License

MIT License

Copyright (c) 2026