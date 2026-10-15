# book-qa-rag-llm
RAG-based book question-answering system using semantic search, vector embeddings, and an LLM to generate context-grounded answers with source references.
# Book Q&A System Using Retrieval-Augmented Generation (RAG)

## Project Overview

This project implements a Retrieval-Augmented Generation (RAG) system that allows users to ask questions about the contents of a book and receive answers based on relevant passages retrieved from the document.

Developed using Python and Google Colab, the system combines semantic search with a language model to retrieve relevant information and generate context-based responses. It also displays source passages, page numbers, and similarity scores to help users trace the information used in an answer.

## Key Features

- **PDF text extraction:** Extracts text from the book using PyMuPDF.
- **Text preprocessing:** Cleans the extracted text and divides it into smaller chunks for efficient retrieval.
- **Vector embeddings:** Converts text chunks and user questions into numerical representations using Sentence Transformers.
- **Semantic search:** Retrieves the most relevant passages by comparing embedding similarity.
- **LLM-based answer generation:** Uses retrieved passages as context for generating answers through a language model.
- **Source references:** Displays relevant page numbers, similarity scores, and text snippets.
- **Context-grounded responses:** Instructs the model to answer using the retrieved context and acknowledge when information cannot be found.

## Technologies Used

- Python
- Google Colab
- PyMuPDF
- Pandas and NumPy
- PyTorch
- Sentence Transformers — `all-MiniLM-L6-v2`
- Hugging Face Transformers
- FLAN-T5-base
- AI-assisted coding

## How It Works

1. Extract text from the source PDF.
2. Clean the text and split it into sentence-based chunks.
3. Generate vector embeddings for the text chunks.
4. Convert the user's question into an embedding.
5. Compare the question embedding with document embeddings to retrieve the top relevant passages.
6. Insert the retrieved passages into a context-based prompt.
7. Generate an answer using FLAN-T5-base.
8. Display the answer alongside retrieved source passages and page references.

## Example Use Cases

- Asking questions about concepts explained in a textbook.
- Finding relevant explanations without manually searching the entire book.
- Supporting self-study and revision.
- Exploring document-based question answering using RAG and LLMs.

## How to Run

1. Open the notebook in Google Colab.
2. Install the required Python libraries.
3. Upload the PDF document you want to query.
4. Run the notebook cells in sequence to extract text, create embeddings, and initialise the language model.
5. Use the `ask_book()` function to ask questions and inspect the generated answers and retrieved sources.

## Role of AI in Development

AI-assisted coding was used to support code development, debugging, and implementation of the RAG workflow. The project provided hands-on experience with document processing, embedding models, semantic retrieval, prompt construction, and language-model-based question answering.

## Limitations

- Answer quality depends on the quality of the source document and retrieved passages.
- Relevant information may be missed if it is not retrieved in the top results.
- Generated answers may be incomplete or inaccurate and should be checked against the cited source passages.
- The notebook requires sufficient memory and processing resources to load the embedding and generation models.

## Project Category

Generative AI | Retrieval-Augmented Generation (RAG) | Natural Language Processing | Semantic Search | AI-Assisted Development
