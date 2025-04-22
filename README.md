# 📄 Doc Fusion

**Doc Fusion** is an automated multi-document summarization tool that processes PDFs and LaTeX files using AI models. It enables efficient information extraction and querying from large text sources. Powered by Google AI Gemini API, Pandoc, and Milvus vector database.

---

## 🚀 Features

- 📚 Multi-PDF summarization with `automation.py`
- 🔍 Searchable knowledge base using vector embeddings
- 🧠 Integration with Gemini API from Google AI Studio
- 📄 Output in PDF & LaTeX format
- 🌐 Streamlit web app interface

---

## 🧰 Installation & Setup

### 🔧 Local Python Setup

python -m venv myenv
.\myenv\Scripts\Activate      # Windows
source myenv/bin/activate     # macOS/Linux

pip install -r requirements.txt

python parse.py
python newparse.py

---

## Milvus Setup with Docker

docker compose up -d

## Connect to Milvus

from pymilvus import MilvusClient, utility, connections

client = MilvusClient(uri="http://localhost:19530", token="root:Milvus")

### Create a test collection
client.create_collection("test", dimension=5)

### List collections
client.list_collections()

### Drop collection
utility.drop_collection("test")

---

## Running the Project

### Summarize documents: 
python automation.py dump .\data\demo.pdf output

### Search a query:
python automation.py search "keyword"

### Run Streamlit UI:
python app.py
streamlit run app.py

---

## 📦 Requirements

- Python 3.10+
- Pandoc (Install from pandoc.org)
- Google AI Studio Gemini API Key
- Docker + Docker Compose
- Milvus Vector Database

---

## 📜 License
MIT License

---

## 🙌 Credits
Developed as a personal project for document intelligence and summarization. Contributions are welcome!
