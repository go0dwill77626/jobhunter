AI Job-Hunter Bot 🤖💼
An automated ETL pipeline that scrapes job listings, evaluates candidate-to-job fit using Google Gemini AI, and delivers real-time notifications via Telegram.🎯
Value Proposition
Passive Sourcing: Automates 10 hours of manual searching per week.
AI Matching: Semantic analysis of resumes vs. job descriptions.
Auto-Drafting: Generates context-aware cover letters for high-match roles.🏗
Technical Architecture
Orchestration: Hosted on GCP Compute Engine using Docker Compose.
Ingestion: Fetches resumes from Google Drive; builds dynamic LinkedIn search queries via JavaScript.
AI Layer: Employs Gemini 1.5 Flash for high-speed scoring (0-100) and structured JSON output.
Sinks: Persists all leads in Google Sheets; alerts on matches >70% via Telegram Bot API.🛠

Tech Stack:
Orchestrator:n8n
LLM: Google Gemini API
Storage: Google Sheets & Drive API
Alerting: Telegram Bot API
Runtime: JavaScript🚀

Quick Start
Import: Copy the job_hunting_bot.json file.
Paste: Ctrl+V into your n8n canvas.
Configure: Add API credentials for Google Cloud, Gemini, and Telegram.
Execute: Set your Cron schedule and run.⚡ Key Features