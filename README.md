# AI Email Support Automation

An automated email triage and response pipeline built with **n8n** and **Google Gemini** that monitors an inbox, analyzes incoming customer queries, and drafts intelligent, contextual email replies[cite: 1].

---

## 📌 Features

- **Inbox Monitoring:** Automatically triggers on new unread support emails via the Gmail API[cite: 1].
- **Intent & Sentiment Analysis:** Uses Google Gemini to detect email sentiment, classify inquiry category, and identify key questions[cite: 1].
- **Contextual Draft Generation:** Drafts professional, accurate replies based on defined support context[cite: 1].
- **Automated Dispatch / Draft Mode:** Can send immediate replies or store generated responses as Gmail drafts for human review.

---

## 🛠️ Tech Stack

- **Automation Engine:** n8n[cite: 1]
- **AI / LLM:** Google Gemini API[cite: 1]
- **Integration:** Gmail API[cite: 1]
- **Data Handling:** JSON, Webhooks, REST APIs[cite: 1]

---

## ⚙️ Workflow Architecture

1. **Trigger:** `Gmail Trigger` listens for incoming emails marked with a specific label or sent to support[cite: 1].
2. **Preprocessing:** Clean HTML body and extract plain text query.
3. **AI Reasoning:** Send message body and system prompt to `Gemini Node` for intent classification and contextual reply drafting[cite: 1].
4. **Execution:** `Gmail Node` creates a draft or automatically replies directly in the existing thread[cite: 1].

---

## 🚀 Setup & Installation

1. Import `workflow.json` into your **n8n** instance.
2. Set up credentials:
   - **Gmail OAuth2** connection[cite: 1].
   - **Google Gemini API Key**[cite: 1].
3. Configure the trigger filter (e.g., target label or sender domain).
4. Turn workflow **Active**.
