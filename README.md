# NativOdds Automated Lead Generation & AI Enrichment Workflow (n8n)

https://jonirar122.app.n8n.cloud/form/7f5c7f9b-33df-4443-b51a-2131482375a8

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

<img width="1600" height="609" alt="WhatsApp Image 2026-09-20 at 3 09 26 PM" src="https://github.com/user-attachments/assets/483a9e03-a087-4dca-8071-aa970d841b46" />

<img width="523" height="325" alt="WhatsApp Image 2026-09-20 at 3 10 47 PM" src="https://github.com/user-attachments/assets/0393acdb-0957-4267-be21-eeb96bfc2b72" />

<img width="1600" height="474" alt="WhatsApp Image 2026-09-20 at 3 13 47 PM" src="https://github.com/user-attachments/assets/819d1b44-4fd3-4199-b9e3-3774af064735" />

<img width="1600" height="482" alt="WhatsApp Image 2026-09-20 at 3 14 09 PM" src="https://github.com/user-attachments/assets/18f79417-7319-4d73-be00-cd2624dd4244" />

<img width="707" height="698" alt="WhatsApp Image 2026-09-20 at 3 14 38 PM" src="https://github.com/user-attachments/assets/ea458cfc-7426-45bb-bd86-0b6430578e5c" />

<img width="590" height="651" alt="WhatsApp Image 2026-09-20 at 3 14 54 PM" src="https://github.com/user-attachments/assets/f81fc513-0cd1-4fb8-83f6-705e56564c77" />


