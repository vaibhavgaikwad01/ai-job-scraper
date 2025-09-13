# 🤖 AI-Powered Job Scraper with Skill Detection

An **AI-powered LinkedIn Job Scraper** that collects job postings based on filters (location, position, experience level, work type, and posting time) and uses **Natural Language Processing (NLP)** to extract required skills from job descriptions.  
The project also provides a **Gradio web interface** for easy use and allows exporting results as CSV files.

---

## 📌 Features
- 🔎 **Job Scraping from LinkedIn**
  - Filter by:
    - Work Type (On-site, Hybrid, Remote)
    - Experience Level (Internship, Entry, Associate, Mid-Senior)
    - Time (Past Day, Past Week, Past Month)
  - Extracts:
    - Job Title, Company, Location, Date, Job Link, Description

- 🧠 **AI Skill Detection**
  - Uses [Flair NLP](https://github.com/flairNLP/flair) (`kaliani/flair-ner-skill`) to automatically detect required skills in job descriptions.

- ⚡ **Background Task Management**
  - Smooth scraping using threading  
  - Stop/reset functionality  
  - Safe concurrent updates  

- 📊 **Data Export**
  - Save results as **CSV files** with timestamps in `saved_jobs/`

- 🌐 **Interactive Web UI**
  - Built with [Gradio](https://gradio.app/)  
  - Real-time scraping progress  
  - Search results displayed in a data table  
  - Option to download data  

---
## 🖼️ Screenshots

### 🔹 Gradio Interface
![Gradio UI](D:\My Projects\DL Projects\ai-job-scraper\screenshots\Interface.png)

### 🔹 Example Job Results
![Job Results](D:\My Projects\DL Projects\ai-job-scraper\screenshots\Output-2.png)
![Job Results](D:\My Projects\DL Projects\ai-job-scraper\screenshots\Output-1.png)


## 🛠️ Tech Stack
- **Python**
- **Web Scraping**: `requests`, `BeautifulSoup`, `urllib3`
- **AI/NLP**: `flair`
- **Data Handling**: `pandas`, `datetime`, `os`
- **Concurrency**: `threading`
- **UI**: `gradio`

---

## 📂 Project Structure
ai-job-scraper/
│── AI_powered_Job_Scrapper.ipynb   # Main notebook
│── requirements.txt                # Dependencies
│── README.md                       # Project documentation
│── saved_jobs/                     # Output CSV files
└── screenshots/                    # Project screenshots



---

## 🚀 How It Works
1. User provides:
   - Cities and States
   - Job Positions
   - Work Types
   - Experience Levels
   - Time Filter
2. Scraper fetches job listings from **LinkedIn**.
3. Each job description is analyzed using **Flair NLP** for skill detection.
4. Results are displayed in the **Gradio interface** and can be **exported to CSV**.

---

## ▶️ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/ai-job-scraper.git
cd ai-job-scraper
### 2. Install Dependencies
pip install -r requirements.txt
### 3. Run the Notebook
jupyter notebook AI_powered_Job_Scrapper.ipynb
