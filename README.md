# 🤖 AI-Powered Job Application Automation Workflow  
### *(n8n + Google Gemini + Google Sheets + Telegram)*

> 🌟 A complete end-to-end **AI + No-Code system** that automates your job search — from **fetching listings** to **writing cover letters**, **tracking applications**, and **sending instant Telegram alerts**.

---

## 🧭 Overview

This project leverages **n8n**, **Google Gemini**, and **Google Sheets** to create a smart job-hunting assistant.  
It automatically:

- 🔍 Fetches job listings from **LinkedIn** or web APIs  
- 🧩 Extracts and structures job data (Title, Company, Location, Description)  
- 🧠 Uses **Google Gemini AI** to write **personalized cover letters**  
- 📈 Assigns a **relevance score** to each opportunity  
- 🧾 Logs job details in **Google Sheets**  
- 📲 Sends **Telegram notifications** for top-scoring roles  

All without writing a single backend script — thanks to **n8n’s no-code automation**!

---

## 🧱 Architecture Overview

```text
[ Scheduler ]
      ↓
[ Download / Extract Jobs ]
      ↓
[ Fetch Jobs from LinkedIn / API ]
      ↓
[ Split Out Jobs ]
      ↓
[ Google Gemini AI Agent ]
      ↓
[ Parse + Append to Google Sheets ]
      ↓
[ Conditional Score Filter ]
      ↓
 ┌───────────────┐
 │ High Score?   │
 └──────┬────────┘
        │
        ├─ Yes → [ Telegram Notification ]
        └─ No  → [ Store + Wait ]


## 🧠 AI-Driven Job Application Workflow
https://raw.githubusercontent.com/TARIFUDDIN/AI-Driven-Job-Application-Automation-n8n-Workflow/main/n8nworkflow.png







⚙️ Workflow Components
Step	Node	Description
1️⃣	Schedule Trigger	Runs the workflow automatically at set intervals
2️⃣	Download & Extract from File	Reads resumes or downloaded job PDFs
3️⃣	Fetch Jobs from LinkedIn / API	Retrieves job listings dynamically
4️⃣	Split Out	Processes each job individually
5️⃣	AI Agent (Google Gemini)	Generates a custom cover letter for each job
6️⃣	Parse AI Output	Cleans up Gemini’s response for display
7️⃣	Append / Update in Google Sheets	Stores job and AI data
8️⃣	IF Condition	Filters top-scoring jobs
9️⃣	Send Telegram Message	Sends alerts for top job matches
🔁	Loop Over Items	Ensures all listings are processed sequentially

🧩 Tech Stack
Category	Tool	Purpose
🧠 AI Model	Google Gemini Chat Model	Generates human-like personalized cover letters
🔄 Automation Engine	n8n	Orchestrates the entire workflow
📊 Database	Google Sheets	Stores job listings & AI-generated outputs
🌐 Data Source	LinkedIn / APIs	Job data retrieval
📱 Notifications	Telegram Bot	Sends job updates directly to the user
🧮 Data Parsing	HTML Extract + JSON Parse	Extracts structured job data


💬 Example Telegram Notification
🚀 New Job Match Found!

💼 Position: MERN Developer  
🏢 Company: Konrad  
📍 Location: Gurgaon, Haryana  
⭐ Score: 96  

🧠 AI Cover Letter:  
"Dear Hiring Team,  
I am writing to express my enthusiastic interest in the MERN Developer position..."

🔗 Apply here: https://www.linkedin.com/jobs/view/...


🛠️ Setup Guide
1. Clone the Repository
git clone https://github.com/<your-username>/ai-job-automation-n8n.git
cd ai-job-automation-n8n


2. Import Workflow

Open your n8n instance

Go to Workflows → Import

Upload workflow/ai-job-automation.json

3. Configure Credentials
Service	Credential	Description
Google Sheets	OAuth / API Key	Read/write data to your job sheet
Telegram Bot	Bot Token	Send job alerts to your Telegram
Google Gemini	API Key	Generate cover letters via Gemini
4. Run the Workflow

Click Execute Workflow in n8n — sit back and watch it:
✅ Fetch jobs → 🧠 Write cover letters → 📊 Save to Sheets → 📲 Notify you on Telegram.

📂 Folder Structure
ai-job-automation-n8n/
├── README.md
├── workflow/
│   └── ai-job-automation.json      # Exported n8n workflow
├── assets/
│   ├── workflow-diagram.png        # Visual overview
│   └── google-sheet-output.png     # Example result
├── scripts/
│   └── sample-prompts.md           # Prompt templates
└── .gitignore


.gitignore

node_modules/
.env
credentials.json
*.log
.DS_Store

🧠 Example Use Case

You can use this workflow to:

Apply to jobs automatically based on skill keywords

Generate personalized cover letters instantly

Track all your applications with scores

Get notified about new relevant openings

Build a personal job intelligence system

🚀 Future Enhancements

✅ Resume keyword matching using AI

✅ Auto-apply to job portals (LinkedIn, Naukri, Indeed)

✅ Integration with Notion / Airtable

✅ Add dashboards for success analytics

✅ Support multiple AI models (Gemini, GPT-4, Claude, etc.)

📸 Screenshots

https://raw.githubusercontent.com/TARIFUDDIN/AI-Driven-Job-Application-Automation-n8n-Workflow-/main/Result-sheets.png
📈 Impact

This workflow demonstrates the real-world power of AI Automation and No-Code tools.
It combines machine intelligence, data organization, and human-like writing to save hours of manual effort.

Highlights

⚡ Fully automated pipeline

💬 Human-quality cover letters

📲 Real-time Telegram alerts

📊 Structured job tracking

🧠 End-to-end AI integration

👨‍💻 Author

Tarifuddin Ahmed
🎓 M.Tech Data Science @ IIT Madras
💡 AI | Automation | Full Stack | Data Science

📬 Connect With Me:

GitHub

LinkedIn

Email

“Don’t search for jobs manually — build systems that find them for you.” 🚀

🪄 License

This project is licensed under the MIT License — free for personal and educational use



