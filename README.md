# PDF RAG ChatBot with Llama2 and Gradio
PDFChatBot is a Python-based chatbot designed to answer questions based on the content of uploaded PDF files. It utilises the Gradio library for creating a user-friendly interface and LangChain for natural language processing.

## Technologies Used 🚀
* Langchain
* Llama2
* ChromaDB
* Hugging Face
* Gradio

## Features ⭐
* Process PDF files and extract information for answering questions.
* Maintain chat history and provide detailed explanations.
* Generate responses using a Conversational Retrieval Chain.
* Display specific pages of PDF files according to the answer.

## Prerequisites 📋
- **Python 3.10 only** (❌ Python 3.12 is not supported due to TensorFlow issues)
- A Hugging Face account and token (for LLaMA 2 or other gated models)

## Usage 📚
1. Upload a PDF file using the "📁 Upload PDF" button.
2. Enter your questions in the text box.
3. Click the "Send" button to submit your question.
4. View the chat history and responses in the interface.
![image](https://github.com/Niez-Gharbi/PDF-RAG-with-Llama2-and-Gradio/assets/57814219/77b76c05-86fe-4020-8c7a-cf3d7402dcfd)

# 📄 PDF_Bot – Ask Questions from Any PDF

**PDF_Bot** is an AI-powered chatbot that lets you upload a PDF and ask questions about its content. It utilises LLMs from Hugging Face, vector-based retrieval with LangChain, and a visually appealing Gradio interface for user interaction.

## 🚀 Features

- ✅ Upload any PDF (text-based)
- 💬 Ask natural language questions
- 📚 Answers are based on actual document context
- ⚙️ Built using LangChain + Hugging Face + Gradio
---
## 📦 Setup Instructions

### 1️⃣ Clone the Repository
git clone https://github.com/aishanirajpal/PDF_Bot.git
cd PDF_Bot

### 2️⃣ Create a Python 3.10 Virtual Environment

py -3.10 -m venv .venv
.\.venv\Scripts\activate

On Mac/Linux:
python3.10 -m venv .venv
source .venv/bin/activate

### 3️⃣ Install Dependencies
pip install -r requirements.txt
⚠️ Includes fixed versions of huggingface_hub, sentence-transformers, torch, and gradio.

🔐 Generate and Use a Hugging Face Token
Step 1: Get your token
👉 https://huggingface.co/settings/tokens

Click “New Token”, name it PDF_Bot, and enable:

✅ Read access to public gated repositories

Step 2: Login using CLI

huggingface-cli login
Then:

Paste the token

Type Y to add as a Git credential

✅ You're now authenticated!

## 🧠 How It Works
src/pdfchatbot.py: Extracts text from your PDF, creates vector embeddings with sentence-transformers, and uses LangChain’s retrieval + generation to answer your queries.

src/app.py: Launches a Gradio UI where users can upload PDFs and chat with the bot.

## 🖥️ Run the Application

python src/app.py
Once running, visit http://127.0.0.1:7860 in your browser.
