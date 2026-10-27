# AI Inbox Agent 🤖

A local AI-powered email automation workflow built using **n8n, Ollama, Llama 3.2, and the Gmail API**. This project automates email classification and reply drafting while keeping email processing and AI inference on a local machine.

## ✨ Features

- **AI Email Classification:** Classifies incoming emails using AI and workflow rules.
- **Automated Reply Drafting:** Generates context-aware email reply drafts using a local LLM.
- **Gmail Integration:** Fetches emails and saves generated replies directly to Gmail Drafts.
- **Processed Email Tracking:** Labels processed emails to help prevent duplicate processing.
- **Scheduled Automation:** Runs automatically according to the configured schedule.
- **Human-in-the-Loop:** Keeps generated replies as drafts for manual review before sending.
- **Local AI Inference:** Uses Ollama to run the language model locally instead of relying on a paid cloud AI API.

## 🛠️ Tech Stack

- **Workflow Automation:** n8n
- **Local LLM Runtime:** Ollama
- **Language Model:** Llama 3.2
- **Email Integration:** Gmail API
- **Containerization:** Docker

## ⚙️ How It Works

1. Fetches incoming emails from Gmail.
2. Processes and classifies emails according to the workflow logic.
3. Selects relevant emails for AI-generated replies.
4. Sends the email context to the locally running Llama 3.2 model.
5. Creates a reply draft in Gmail.
6. Applies a processing label to the original email to reduce duplicate processing.

## 🚀 Getting Started

### Prerequisites

Before running the workflow, ensure you have:

- Docker Desktop installed.
- Ollama installed and running.
- The `llama3.2` model downloaded in Ollama.
- An n8n instance running locally.
- A Gmail account with OAuth2 credentials configured in n8n.

### Setup

1. Clone or download this repository.
2. Start Ollama and ensure the `llama3.2` model is available.
3. Start your local n8n instance.
4. Import `AI-Inbox-Agent.json` into n8n.
5. Configure the required Gmail OAuth2 credentials in n8n.
6. Verify the Ollama connection and update the model endpoint if necessary.
7. Review the workflow configuration and schedule.
8. Test the workflow with sample emails before enabling automatic execution.

## 🔒 Security and Privacy

- Configure Gmail credentials directly in your local n8n instance.
- Never commit OAuth tokens, client secrets, passwords, or private email content.
- Review the exported workflow JSON before publishing it publicly.
- Generated replies are saved as drafts and are not sent automatically.
- Local AI inference does not require sending email content to a cloud-based LLM API, although Gmail itself remains an external service.

## 📂 Repository Structure

```text
AI-Inbox-Agent/
├── AI-Inbox-Agent.json
└── README.md
```

## 🎯 Project Goal

The goal of this project is to demonstrate how local large language models and workflow automation can be combined to build a practical AI email assistant that reduces repetitive email work while preserving human control over outgoing messages.

## 👨‍💻 Author

**Ahmed Iftikhar**

[GitHub Repository](https://github.com/AhmedIftikhar02/AI-Inbox-Agent)
