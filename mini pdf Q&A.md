# 📄 Mini PDF Q&A Demo

A simple AI-powered **PDF Question & Answer application** built with **Python, Streamlit, PyMuPDF, and OpenAI**.

The application allows users to upload a PDF document, extracts its text, and lets them ask questions about the document using an OpenAI language model.

## 🚀 Features

* 📤 Upload PDF documents directly from the web interface
* 📖 Extract text from PDF files using **PyMuPDF**
* 💬 Ask questions about the uploaded document
* 🤖 Generate AI-powered answers using **OpenAI**
* ⚡ Simple and interactive **Streamlit** interface
* 🔍 Lightweight implementation without a vector database

## 🛠️ Technologies Used

| Technology     | Purpose                       |
| -------------- | ----------------------------- |
| Python         | Application development       |
| Streamlit      | Web interface                 |
| PyMuPDF (fitz) | PDF text extraction           |
| OpenAI API     | AI-powered question answering |

## 📂 Project Structure

```text
document-main/
│
├── README.md
├── app.py
└── requirements.txt
```

> The main Python file may have a different filename in your local project. Replace `app.py` above if necessary.

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd document-main
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

On macOS/Linux:

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install streamlit pymupdf openai
```

Or, if a `requirements.txt` file is available:

```bash
pip install -r requirements.txt
```

## 🔑 OpenAI API Key

The application requires an OpenAI API key.

**Do not store your API key directly in the source code or upload it to GitHub.**

Instead, use an environment variable or Streamlit secrets.

### Using an environment variable

Windows PowerShell:

```powershell
$env:OPENAI_API_KEY="your-api-key"
```

macOS/Linux:

```bash
export OPENAI_API_KEY="your-api-key"
```

Then access it in Python using:

```python
import os

api_key = os.getenv("OPENAI_API_KEY")
```

### ⚠️ Security Notice

If an actual API key has ever been committed to a public or shared repository, **revoke/rotate that key immediately** and create a new one.

## ▶️ Run the Application

Start the Streamlit application with:

```bash
streamlit run app.py
```

Streamlit will provide a local URL, typically:

```text
http://localhost:8501
```

Open the URL in your browser.

## 📖 How It Works

The application follows these basic steps:

```text
        Upload PDF
             ↓
     Extract PDF Text
             ↓
      Enter Question
             ↓
   Send Context + Question
        to OpenAI
             ↓
       Generate Answer
             ↓
        Display Answer
```

### 1. Upload PDF

The user uploads a PDF through Streamlit's file uploader.

### 2. Extract Text

PyMuPDF reads the PDF and extracts text from each page.

### 3. Ask a Question

The user enters a question related to the uploaded document.

### 4. Generate Answer

The extracted document text and question are sent to the OpenAI model.

### 5. Display Result

The generated answer is displayed directly in the Streamlit interface.

## 💡 Example

After uploading a PDF containing a research paper, a user could ask:

```text
What is the main objective of this research?
```

The application processes the document and generates an AI-based answer.

Other possible questions:

* What are the key findings?
* Summarize this document.
* What methodology was used?

