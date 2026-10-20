# RAG QA Chatbot for Insurance Documents  
Effortless Question Answering on Insurance Documents Powered by RAG and Gemini Flash Model  

---  

## ✨ About the Project  
The RAG QA Chatbot is a robust solution for answering queries on insurance documents. Understanding and interpreting large, complex insurance policies can be challenging. This chatbot simplifies the process by combining document retrieval techniques with advanced generative AI models, delivering accurate answers in real-time.  

---  

## 🔍 Key Features  
- 🌟 **Accurate Responses**: Uses a Retrieval-Augmented Generation (RAG) pipeline to ensure precise answers.  
- ⚡ **Efficient Embedding Storage**: Leverages **ChromaDB** for fast, scalable embedding storage and retrieval.  
- 🧠 **AI-Powered Generation**: Combines OpenAI embeddings with Gemini Flash Model for high-quality answer generation.  
- 🛠️ **Caching Mechanisms**: Implements cache layers for:  
  - Embedding storage to avoid reprocessing identical documents.  
  - Query responses to skip re-evaluating repeated questions.  
- 📄 **Page-Level Chunking**: Splits documents into manageable sections for optimal retrieval performance.  
- 🤖 **Real-Time Interaction**: Instantly retrieves and processes relevant document sections for user queries.  

---  

## 🛠️ Tech Stack  
- **Language**: Python  
- **Frameworks/Libraries**: PDFPlumber, ChromaDB, Pandas, Numpy, Torch, Transformers
- **APIs/Models**:  
  - Sentence Transformers Embedding Model for creating vector embeddings  
  - Gemini Flash Model for generating user responses  

---  

## 🧪 Example Use Cases
- "What is the claim process for health insurance?"  
- "Does this policy cover accidental damage?"

---

## 📸 Sample Output
### 1. Sample Code Output
![Sample Code Output](Code%20Sample%20Output%20Screenshots/Code%20Sample%20Output%202.png)

### 2. Sample Code Output Cache Response
![Sample Code Output Cache Response](Code%20Sample%20Output%20Screenshots/Code%20Sample%20Output%201.png)

---

## 🚀 Getting Started

### Prerequisites
Ensure you have the following installed:
- Python 3.8+

### Installation

1. Navigate to the project directory:
cd Insurance_Document_Chatbot_RAG

2. Install the required dependencies:
pip install -r requirements.txt

- Please note: OpenAI/Gemini API keys are required for the project to function. You can obtain them from their websites and change the same in the code.

4. Run the main file from Jupyter environment:
"Insurance_Document_Chatbot_RAG.ipynb"

---

## 🛠️ Challenges/Issues Faced with fixes
- [Issue #1](For Preprocessing PDF file, many tools like PDFminer, PyPDF2 etc was tried, but they were not suitable for the task. PDFplumber was finally chosen.)
- [Issue #2](Extracting Tables from PDF was also a challenge. Whole data processing logic was reworked with PdfPlumber to extract the data from tables in readable format and then appended in the correct sequence.)
- [Issue #3](Cache layer was added in ChromaDB to prevent re-embedding of the same documents. This was done to avoid overloading the ChromaDB server with data and to make the retrieval process more efficient.)
- [Issue #4](Another Cache layer was added to prevent re-search of the same queries. This was done to make the retrieval process more efficient.)
- [Issue #5](Cross Encoder based Reranker was added to better select the most relevant passages from the document. This was done to improve the quality of the answers to the user queries.)
- [Issue #6](Hardcoded API keys were replaced with input from user. This was done to make the project more secure and user-friendly.)
- [Issue #7](Embedding generation using ChromaDB's Default model was replaced by OpenAI's Embedding Model. This was done to improve the quality of the answers to the user queries.)
- [Issue #8](Changed 'Tempearture' parameter of OpenAI's Embedding Model to 0.1. This was done to improve the quality of the answers to the user queries so that the model doesn't generate irrelevant answers and produces reproducible and consistent results.)

---

## 🚀 Future Scope
- Expand support for multi-language documents and queries.
- Add support for file formats beyond PDF.
- Add Support for more LLM models like ChatGPT and Claude AI.

---

## 📖 Documentation
No documentation will be made available for this project since this project only uses technologies that already have their own documentation. Please refer to the following links for more information:
- [Gemini](https://ai.google.dev/gemini-api/docs/models/gemini)
- [ChromaDB](https://docs.trychroma.com/)
- [PDFPlumber](https://pypi.org/project/pdfplumber/0.1.2/)
- [Pandas](https://pandas.pydata.org/docs/)
- [transformers](https://huggingface.co/docs/transformers/index)
- [torch](https://pytorch.org/docs/stable/index.html)
- [Numpy](https://numpy.org/doc/stable/)

---

## 🛡️ Conclusion 
The RAG QA Chatbot for Insurance Documents provides a powerful and efficient way to extract valuable information from complex insurance policies. By combining state-of-the-art retrieval and generation techniques with intelligent caching and document chunking strategies, this solution ensures fast, accurate, and relevant responses to user queries. Whether you are dealing with claim processes, coverage details, or policy exclusions, this chatbot can quickly and effectively guide you through the information you need.  

This project serves as a solid foundation for building intelligent document-based chatbots and showcases the potential of combining retrieval-augmented generation with modern AI models.  
 
---
