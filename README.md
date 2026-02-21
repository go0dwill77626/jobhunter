# AI Job-Hunter Bot 🤖💼

An automated ETL pipeline that scrapes job listings, evaluates candidate-to-job fit using **Google Gemini AI**, and delivers real-time notifications via **Telegram**.

## 🎯 Value Proposition
* **Passive Sourcing:** Automates ~10 hours of manual searching and filtering per week.
* **AI Matching:** Performs deep semantic analysis of resumes vs. job descriptions.
* **Auto-Drafting:** Generates context-aware, tailored cover letters for roles with high-match scores.

## 🏗 Technical Architecture
The system is built as a containerized microservice architecture:
* **Orchestration:** Self-hosted on **GCP Compute Engine** using **Docker Compose**.
* **Ingestion:** Fetches resumes from **Google Drive**; builds dynamic LinkedIn search queries via **JavaScript** nodes.
* **AI Layer:** Employs **Gemini 1.5 Flash** for high-speed scoring (0-100) and structured JSON output.
* **Sinks:** Persists all leads in **Google Sheets**; triggers alerts for matches >70% via the **Telegram Bot API**.



## 🚀 Tech Stack
| Component | Technology |
| :--- | :--- |
| **Orchestrator** | n8n |
| **LLM** | Google Gemini API (1.5 Flash) |
| **Storage** | Google Sheets & Drive API |
| **Alerting** | Telegram Bot API |
| **Runtime** | Node.js / JavaScript |

## ⚡ Quick Start
1. **Import:** Copy the `job_hunting_bot.json` file from this repo.
2. **Paste:** Use `Ctrl+V` to import directly into your n8n canvas.
3. **Configure:** Add your API credentials for Google Cloud, Gemini, and Telegram in the n8n Credentials screen.
4. **Execute:** Set your Cron schedule node and hit 'Execute Workflow'.

---
*Developed by [go0dwill77626](https://github.com/go0dwill77626)*