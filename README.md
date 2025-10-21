# Janus

**Janus** is an AI-powered helpdesk system that makes customer support faster and smarter. It helps users raise support tickets, get instant AI replies, and lets admins manage everything from one simple dashboard.

## Use Case

Enterprise helpdesks spend hours triaging and responding to repetitive support requests.
Janus automates the lifecycle:

- Users submit tickets and chat with an AI support agent in real time.
- The system classifies intent, priority, and category automatically.
- Admins can visualize ticket trends, approve high-value cases into the Knowledge Base, and run searches across historical data.

**Result:** Reduced response time, consistent resolutions, and actionable insights.

## Features

**🎟️ User Portal**

- Submit new support tickets.
- Get an instant AI-generated first response.
- Chat with the AI about your issue.
- View all your previous tickets in one place.

**🧠 Admin Portal**

- View visual dashboards showing ticket trends.
- Review and manage tickets — approve useful ones for the Knowledge Base or delete them.
- Search the Knowledge Base using filters like priority, type, or category.

**🤖 AI Agents**

1. Ticket Classifier

- Predicts ticket type, category, tags, and priority.
- Learns from past tickets to improve classification accuracy over time.

2. Support Agent

- Generates the first AI response for every new ticket.
- Handles ongoing chats with users to resolve their issues.
- Uses the tickets knowledge base for context and better answers.

## Technology

- [Python](https://www.python.org/) (Best Programming Language :P)
- [Streamlit](https://streamlit.io/) (UI Library)
- [MindsDB](https://mindsdb.com/) (AI and KB Layer)
- [ChromaDB](https://www.trychroma.com/) (Vector DB)
- [Nebius](https://nebius.com/) (For LLM and Embedding model)

## Installation

1. Clone the github repository

```bash
git clone https://github.com/k0msenapati/janus.git
cd janus
```

2. Download the dataset

```bash
# Create data directory if not exists
mkdir -p data

# Download dataset zip via Kaggle API
curl -L -o data/customer-support-tickets.zip \
  https://www.kaggle.com/api/v1/datasets/download/tobiasbueck/multilingual-customer-support-tickets

# Unzip contents to data directory
unzip -o data/customer-support-tickets.zip -d data

# Optional: remove the zip after extraction
rm data/customer-support-tickets.zip
```

3. Setup project, environment variables and run setup script

```bash
uv sync

cp .env.example .env # add your nebius api key from nebius ai cloud to NEBIUS_API_KEY var

uv run setup.py
```

4. Run Streamlit App

```bash
source .venv/bin/activate
streamlit run app.py
```

## Author

Built with 💖 by [k0msenapati](https://github.com/k0msenapati)
