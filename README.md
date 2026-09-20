# NativOdds Automated Lead Generation & AI Enrichment Workflow (n8n)

An automated agency lead processing pipeline built using **n8n workflow automation**, **Gemini AI API**, **Custom HTML/JavaScript Scripts**, **Google Sheets**, and automated email nodes.

---

## 📌 Project Overview
This project provides a complete end-to-end automation solution for agency inquiry management built on n8n. As soon as a potential client submits a web contact form, the workflow automatically logs raw submission data, generates a tracking ID, analyzes project requirements using Gemini AI, updates central database records, and dispatches responsive HTML emails to both the client and internal agency teams.

---

## ⚡ Key Features

* **Trigger Node & Entry Point:** Captures real-time form submissions containing client details (Name, Email, Phone, Budget, and Project Description).
* **Unique Identification Generator:** Uses a custom code script to automatically generate a unique tracking ID (e.g., `LEAD-1789897603480-TX1QX7`) for each inquiry.
* **Initial Data Logging:** Instantly inserts raw inquiry data as a new row into Google Sheets via the n8n Google Sheets node.
* **AI Processing & Enrichment (Gemini AI Node):**
  * Analyzes project descriptions and budget constraints.
  * Automatically generates **Lead Score** (High / Low), **Category**, **Recommended Tech Stack**, **Estimated Effort**, **Client Intent Analysis**, and **Next Action Steps**.
* **AI Data Syncing:** Matches the unique Lead ID row in Google Sheets and updates it with AI-generated insights.
* **Automated Email Dispatch:**
  * **Customer Confirmation:** Sends a professionally designed HTML receipt email to the client with submission reference details.
  * **Internal Alert / Notification:** Sends a detailed alert to the internal agency team containing lead details and AI evaluation scores for quick follow-up.
* **Final Status Update:** Automatically updates the `Email Status` column in Google Sheets to **Sent** once emails are successfully delivered.

---

## 🛠️ Workflow Steps in n8n

1. **On form submission** ➔ Triggers the workflow upon receiving lead input.
2. **Generate Lead ID** ➔ Executes JS/HTML script node to create unique tracking code.
3. **Append row in sheet** ➔ Logs raw input data into Google Sheets.
4. **Message a model (Gemini AI)** ➔ Processes client project prompt & returns structured evaluation.
5. **Update row in sheet** ➔ Syncs AI output to the spreadsheet under the matching Lead ID.
6. **Send a message (Dual Emails)** ➔ Dispatches client confirmation & internal team alert.
7. **Update row in sheet1** ➔ Updates email delivery status to `Sent`.

---

## 🚀 Tech Stack & Tools

* **Workflow Automation Engine:** n8n
* **AI Engine:** Google Gemini AI Model
* **Scripting / Logic:** JavaScript / HTML Scripts (Code Nodes)
* **Database / Storage:** Google Sheets API
* **Email Protocol:** SMTP / Mail Service Nodes
* **Frontend Design:** Custom Responsive HTML/CSS Email Templates
