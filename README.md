
# 📄 Data Harvest & Document Processor for Sanskrit and Cultural Archives

This repository contains a web scraping and document processing pipeline built using Python, designed to crawl websites, download cultural and Sanskrit-related documents (PDF/EPUB/HTML), extract and normalize metadata, perform OCR on scanned files (including **Sanskrit and Hindi**), and output structured metadata in JSON format.

---

## 📌 Features

- ✅ Website crawling and parsing with `BeautifulSoup` and `requests`
- ✅ Follows `robots.txt` rules
- ✅ Downloads documents in `.pdf`, `.epub`, `.html`, and `.htm` formats
- ✅ Computes file checksums (SHA256) to avoid duplication
- ✅ Extracts metadata (title, author, etc.) from PDF metadata
- ✅ Performs OCR on scanned documents using **Tesseract** (supports **Sanskrit** and **Hindi**)
- ✅ Normalizes and stores metadata into structured JSON format
- 🛠️ Currently, **title, author, etc. extraction from content is not implemented successfully**, only extracted from PDF metadata

---

## 🧾 Requirements

Ensure the following Python packages are installed before running the notebook:

```txt
beautifulsoup4
requests
python-docx
PyMuPDF
pdf2image
pytesseract
tika
tqdm
```

You can install all dependencies using:

```bash
pip install -r requirements.txt
```

Make sure **Tesseract-OCR** is installed and available in your system PATH.

- On Ubuntu/Debian:

  ```bash
  sudo apt update && sudo apt install tesseract-ocr tesseract-ocr-san tesseract-ocr-hin
  ```

- On Windows, download from [Tesseract GitHub](https://github.com/tesseract-ocr/tesseract) and configure the path.

---

## 📁 Directory Structure

```bash
.
├── Data_Harvest_Unidox.ipynb    # Main Notebook
├── requirements.txt             # Dependencies
├── data/                        # Downloaded files (created during runtime)
├── output/                      # Extracted metadata JSON
└── README.md                    # You're reading this!
```

---

## ⚙️ How to Use

1. Clone the repo:

   ```bash
   git clone https://github.com/yourusername/unidox-data-harvest.git
   cd unidox-data-harvest
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook:

   ```bash
   jupyter notebook Data_Harvest_Unidox.ipynb
   ```

4. Configure your target URL(s) inside the notebook and run all cells.

---

## 🧠 Notes

- OCR is optimized for **Sanskrit and Hindi** documents.
- Extraction of **author names from document content** is currently **not functional**. Metadata is fetched from file metadata where available.
- All non-text documents are converted to image format (if needed) before OCR.

---

## 🔍 Example Output (Metadata JSON)

```json
{
  "file_name": "ancient_text.pdf",
  "title": "Rigveda Commentary",
  "author": "Unknown",
  "checksum": "a3bc...7e1",
  "language": "sa",
  "extracted_text": "...",
  "source_url": "http://example.com/rigveda"
}
```

---

