# 📊 Automated Scheduled Data Summarization & Logic Routing

An efficient, no-code automation workflow built with **n8n**. This system is designed to autonomously fetch periodic data, aggregate it into a concise summary, and perform conditional routing based on business logic.

## ⚙️ Workflow Architecture
As shown in the technical flow:
1. **Schedule Trigger:** The workflow initiates automatically at a predefined time.
2. **Data Extraction (Google Sheets):** Fetches multiple raw data entries (7 items) from a centralized spreadsheet.
3. **Data Aggregation (Summarize Node):** Transforms the raw entries into a single, consolidated summary (1 item) to ensure clean reporting.
4. **Primary Notification:** Sends an initial summary email to the supervisor.
5. **Conditional Logic (IF Node):** Evaluates the summarized result against a specific threshold.
6. **Smart Routing:** - **True Path:** Triggers a "Target Met" confirmation email.
   - **False Path:** Triggers an "Action Required" alert email.

## 🛠️ Tech Stack
* **n8n** (Workflow Automation)
* **Google Sheets API** (Data Source)
* **Gmail/SMTP** (Communication)
* **Logical Routing** (Conditional Branching)

## 🚀 Key Features
* **Zero-Touch Automation:** Runs 100% independently on a schedule.
* **Smart Summarization:** Reduces noise by aggregating multiple data points before delivery.
* **Dynamic Communication:** Adapts the email content based on real-time data results.

## 📂 Installation
1. Download the `workflow.json` file.
2. Import it into your **n8n** instance.
3. Connect your **Google Sheets** and **Gmail** credentials.
