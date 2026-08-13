

🤖 LangBot — An Advnace AI Assistant

> **A conversational AI assistant built to go beyond simple chat — combining RAG, persistent memory, intelligent tools, and an interactive interface into one unified experience.**

LangBot is an AI-powered conversational assistant developed as a collaborative project. It combines **Retrieval-Augmented Generation (RAG)**, long-term conversational memory, external tools, and a modern interactive interface to create a more capable and context-aware AI experience.

The project explores how Large Language Models can be connected with external data, databases, APIs, and tools to create assistants that can **remember, retrieve, reason, and respond**.

---

## ✨ What Makes LangBot Different?

Traditional chatbots generally respond only to the current conversation.

LangBot extends that idea by giving the assistant access to:

* 🧠 **Long-term conversational memory**
* 🔎 **Retrieval-Augmented Generation (RAG)**
* 🛠️ **Tool-based capabilities**
* 🗄️ **Persistent data storage**
* 🔗 **External APIs**
* 📊 **Conversation analytics**
* 💬 **Interactive chat experience**

This creates an assistant that is designed to be more **context-aware, useful, and extensible**.

---

## 🚀 Key Features

### 🧠 Context-Aware Conversations

LangBot maintains conversation context using persistent memory, allowing interactions to feel more continuous rather than treating every query as an isolated request.

### 🔍 Retrieval-Augmented Generation

The RAG pipeline allows the system to retrieve relevant information before generating a response, helping the assistant provide more contextually grounded answers.

### 🛠️ Intelligent Tool Integration

LangBot can interact with multiple utilities instead of relying exclusively on the language model.

Integrated tools include:

* 🌦️ Weather information
* 📈 Stock price information
* 🔎 Web/search functionality
* 🧮 Mathematical calculations

### 💾 Persistent Memory

PostgreSQL is used to maintain conversational information, allowing the assistant to preserve relevant context across interactions.

### 🎨 Interactive Interface

The application provides a clean conversational interface with features such as:

* Chat interface
* Conversation history
* Dark mode
* Analytics panel
* Real-time responses

---

## 🏗️ System Overview

The project follows a modular architecture where the user interface communicates with the AI/backend layer, which coordinates memory, retrieval, and external tools.

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Streamlit UI      │
                    │  Chat & Analytics   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  AI / Agent Layer   │
                    │ LangChain / LangGraph│
                    └──────┬──────┬───────┘
                           │      │
             ┌─────────────┘      └──────────────┐
             ▼                                    ▼
    ┌─────────────────┐                  ┌─────────────────┐
    │ RAG / Retrieval │                  │ External Tools  │
    │    ChromaDB     │                  │ Search / Weather│
    └─────────────────┘                  │ Stock / Math    │
                                         └─────────────────┘
             │
             ▼
    ┌─────────────────┐
    │   PostgreSQL    │
    │ Persistent Memory│
    └─────────────────┘

                    ┌─────────────────┐
                    │   LangSmith     │
                    │ Observability    │
                    └─────────────────┘
```

---

## 🧰 Technology Stack

| Category        | Technologies                   |
| --------------- | ------------------------------ |
| Programming     | Python                         |
| Frontend        | Streamlit, HTML, CSS           |
| AI Framework    | LangChain, LangGraph           |
| Generative AI   | Large Language Models          |
| RAG             | Retrieval-Augmented Generation |
| Vector Database | ChromaDB                       |
| Database        | PostgreSQL                     |
| Observability   | LangSmith                      |
| APIs            | External tool/API integrations |

---

## 👩‍💻 My Contribution

This project was developed collaboratively as a **2-member team**.

### My Role — Frontend Developer

I was primarily responsible for the frontend experience and its integration with the backend services.

My contributions included:

* Designed and developed the **Streamlit-based user interface**.
* Built the conversational chat interface.
* Implemented **conversation history** functionality.
* Developed the **analytics panel**.
* Added and customized the application's **dark mode**.
* Integrated frontend components with backend APIs.
* Worked with the backend team to align API responses and data formats.
* Debugged API integration issues and improved the overall user experience.

---

## 🔄 How LangBot Works

A typical interaction follows this flow:

```text
User Query
    ↓
Streamlit Interface
    ↓
AI Agent
    ↓
Understand User Intent
    ↓
┌──────────────────────────────┐
│                              │
▼                              ▼
Retrieve Context          Select Tool
│                              │
▼                              ▼
RAG / Memory              API / Utility
│                              │
└──────────────┬───────────────┘
               ▼
        Generate Response
               ↓
        Display to User
```

The agent determines whether a request requires conversational context, retrieved information, or an external tool before producing the final response.

---

## 📂 Project Structure

```text
LangBot/
│
├── frontend/
│   ├── components/
│   ├── pages/
│   └── ...
│
├── backend/
│   ├── agents/
│   ├── tools/
│   ├── memory/
│   └── ...
│
├── database/
│   └── ...
│
├── requirements.txt
├── README.md
└── ...
```

> **Note:** Update the folder names above if your repository uses a different structure.

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/rounak3110/LangBot-An-AI-ChatBot.git
cd LangBot-An-AI-ChatBot
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**macOS / Linux**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file and add the required API credentials and database configuration.

Example:

```env
OPENAI_API_KEY=your_api_key
DATABASE_URL=your_database_url
```

> Do not commit API keys, passwords, database credentials, or other secrets to GitHub.

### 5. Run the application

```bash
streamlit run app.py
```

The application should then be available locally through the Streamlit server.

---

## 🎯 Learning Outcomes

Building LangBot provided practical exposure to:

* Generative AI application development
* Retrieval-Augmented Generation
* AI agent workflows
* Conversational memory
* Vector databases
* API integration
* PostgreSQL
* Frontend development with Streamlit
* Backend/frontend communication
* Debugging distributed application components
* Observability using LangSmith
* Collaborative software development

---

## 🔮 Possible Future Enhancements

Some potential directions for extending LangBot include:

* 🔐 User authentication and personalized profiles
* 📄 Document upload and private knowledge bases
* 🎙️ Voice-based interaction
* 🌐 Multi-language conversations
* 🧩 Additional tool integrations
* 📱 Mobile-friendly interface
* 📊 More detailed conversation analytics
* 🧠 Improved memory management and personalization

---

## 🤝 Team Project

LangBot was developed collaboratively as a 2-member project, with responsibilities divided across frontend and backend development.

The project provided hands-on experience in taking an AI application from individual components to an integrated conversational system.

---

## 📌 Project Highlights

**Project Type:** Generative AI / AI Assistant
**Development Model:** Collaborative Team Project
**Primary Language:** Python
**Frontend:** Streamlit
**Architecture:** RAG + Agentic Workflow + Persistent Memory
**Database:** PostgreSQL + ChromaDB

---


