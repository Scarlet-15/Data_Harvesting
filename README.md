# 📄 Data Harvest and Document Extraction Pipeline

This project automates the crawling, downloading, and processing of cultural and government documents (PDF, DOCX, EPUB, HTML). It extracts structured metadata and text content, with OCR support for scanned files including Sanskrit and Hindi documents.

---

## 🚀 Features

- 🌐 Crawl and download supported documents from websites
- 📄 Supported formats: `.pdf`, `.epub`, `.docx`, `.html`
- 🧾 Extract text content using direct parsing or OCR
- 🪪 Extract metadata from files (title, author, etc.)
- 🔐 Compute checksums (SHA256) for file integrity
- 📚 OCR engine supports **Sanskrit** and **Hindi** scripts
- 🗂 Normalize output as structured JSON records

---

## ⚙️ Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
