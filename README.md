# AI Email Reply Automation with n8n

This project is a no-code/low-code email automation workflow built using **n8n**, designed to automatically read incoming Gmail messages, generate professional replies using a **Groq AI agent**, and send those replies with contextual awareness and memory capabilities.

---

## 📌 Features

- ✅ Automatically fetches unread Gmail messages
- 🤖 Uses an advanced AI model (LLaMA 3 via Groq) to generate context-aware replies
- 🧠 Includes conversation memory for coherent follow-ups
- 📬 Sends polite, professional email replies tailored to the sender's intent
- 🔁 Can be scheduled or triggered manually
- 🧩 Built entirely using open-source n8n workflow

---

## 🧠 Workflow Overview

1. **Trigger**: Manually or via scheduling (e.g., every 5 minutes)
2. **Fetch Email**: Get unread Gmail messages
3. **Extract Email Details**: Retrieve full content, sender, subject, and snippet
4. **Prompt AI**: Send the email snippet to the Groq-based AI with prompt engineering
5. **Memory Integration**: Maintain conversation memory for contextual replies
6. **Generate Reply**: AI composes a professional, human-like reply
7. **Send Response**: Reply is emailed back to the original sender

---

## 🚀 Technologies Used

| Tool            | Purpose                                   |
|-----------------|-------------------------------------------|
| n8n             | Workflow automation platform              |
| Gmail Node      | Read/send emails                          |
| Langchain Agent | Advanced reasoning and prompt handling    |
| Groq Chat Model | LLaMA3-based high-speed AI reply generation |
| Memory Buffer   | Stores session context per email thread   |

---

## 📁 Folder Structure

```bash
📦ai-email-auto-reply
 ┣ 📄 My_workflow.json       # Main n8n workflow
 ┗ 📄 README.md              # Documentation (you are here)
