# Agentic_AI_Tech_Newsletter

# 🧠 AI-Powered Tech News Reader with Weekly Summary - n8n Workflow

This repository contains an automated workflow built with **n8n** that allows AI to read tech news daily and send personalized weekly summaries to your email.

---

## 📌 Use Case: Let AI Read the Tech News for You

### 🎯 Goal
Automatically track, summarize, and email the most relevant tech news to the user using AI (OpenAI) and workflow automation (n8n).

---

## 🔁 Workflow 1: Save News in a Vector Store (Runs Daily)

### 🔧 Purpose
Collects and stores tech news articles in an AI-friendly format (vector embeddings) for later summarization.

### 🧩 Process
1. **Trigger**: `Get Articles Daily` – Initiates the process daily.
2. **Set RSS Feeds**: `Set Tech News RSS Feeds` – Manually define RSS feed sources.
3. **Split Feeds**: `Split Out` – Splits multiple feed URLs.
4. **Read Feeds**: `Read RSS News Feeds` – Reads articles from each feed.
5. **Normalize Fields** – Extracts consistent structure: title, content, metadata.
6. **Embed Articles**: `Embeddings OpenAI`
   - Transforms articles into embeddings for semantic search.
   - Handles large articles using a `Recursive Character Text Splitter`.
7. **Store Articles**: `Store News Articles` – Stores articles in a vector store.

---

## 📬 Workflow 2: Send a Summary (Runs Weekly)

### 🔧 Purpose
Uses OpenAI to generate a personalized summary and emails it to the user.

### 🧩 Process
1. **Trigger**: `Send Weekly Summary` – Executes once a week.
2. **User Preferences**: `Your topics of interest` – Define topics (e.g., AI, Google, SpaceX).
3. **News Reader Agent**: Uses OpenAI’s Chat Model and vector store to generate summaries.
4. **Format Email**: Converts summary into an HTML email.
5. **Send Newsletter**: Sends it via Gmail.

---

## ⚙️ How to Use

1. Connect your OpenAI and Gmail accounts in n8n.
2. Customize the RSS feeds in `Set Tech News RSS Feeds` node.
3. Define your interests in `Your topics of interest` node.
4. Enable both workflows and set them on schedule.

---

## ✅ Requirements

- OpenAI credentials (for embeddings and summarization)
- Gmail or SMTP credentials (for sending emails)
- RSS feeds list

---

## 📈 Benefits

- Automated daily tracking of tech news.
- AI-curated summaries based on your interests.
- Weekly email digest of the most relevant tech stories.

---
