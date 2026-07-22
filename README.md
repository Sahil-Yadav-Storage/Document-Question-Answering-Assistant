# Document-Question-Answering-Assistant
An end to end RAG Document Question Answering Assistant built from scratch without high-level orchestration frameworks
Features & Implementation Details
No Frameworks: Built strictly using native Python data structures and low-level ML libraries.

Text Extraction: Reads PDF documents page-by-page using pypdf.

Custom Chunking: Character-based chunking with a 500-character window and 50-character sliding overlap.

Vector Indexing: Converts text chunks into vector embeddings using sentence-transformers (all-MiniLM-L6-v2).

NumPy Similarity Search: Normalizes vectors and computes cosine similarity via dot products using numpy to retrieve the top 3 relevant chunks per query.

Local LLM Integration: Employs Qwen/Qwen2.5-1.5B-Instruct via Hugging Face transformers for response generation on GPU.

Conversation Memory (Bonus): Maintains multi-turn conversation history across queries without bloating context length.

System Requirements
Platform: Google Colab

Hardware Accelerator: T4 GPU (Required for running the local LLM smoothly)
Setup & Execution Instructions
Step 1: Set Up Google Colab Hardware Acceleration
Open a new Google Colab notebook (.ipynb).

Go to the top menu and select Runtime > Change runtime type.

Under Hardware accelerator, select T4 GPU.

Click Save.
Step 2: Add Code Cells & Run
Run the cells in order
Cell 1: Install Dependencies
Cell 2: input the asked file
Cell 3 Wait for memory to be built
Cell 4: Ask questions

Session Management Instructions
To exit the chat: Type exit or quit into the input prompt.

To resume chatting (Keep memory): Re-run Cell 4.

To clear conversation memory (Start fresh): Re-run Cell 3, then run Cell 4.
